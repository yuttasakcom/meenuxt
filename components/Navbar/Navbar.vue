<template>
    <div>
        <nav>
            <div class="nav-wrapper container">
                <nuxt-link to="/" class="brand-logo">DevMeetup</nuxt-link>
                
                <a href="#" data-activates="slide-out" class="button-collapse">
                   <i class="material-icons">menu</i>
                </a>

                <ul class="right hide-on-med-and-down">
                    <nuxt-link
                        tag="li"
                        v-for="item in menuItems"
                        :key="item.title"
                        :to="item.to"
                    >
                        <a>
                            <i class="material-icons left">{{ item.icon }}</i>{{ item.title }}
                        </a>
                    </nuxt-link>
                </ul>
            </div>
        </nav>

        <SideNav :menuItems="menuItems" />
    </div>
</template>

<script>
import SideNav from './SideNav'
export default {
  components: {
    SideNav
  },
  data() {
    return {
      menuItems: [
        { icon: 'supervisor_account', title: 'View Meetups', to: '/meetups' },
        { icon: 'room', title: 'Organize Meetup', to: '/meetups/new' },
        { icon: 'person', title: 'Profile', to: '/users/profile' },
        { icon: 'face', title: 'Sign up', to: '/users/signup' },
        { icon: 'lock_open', title: 'Sign in', to: '/users/signin' }
      ]
    }
  }
}
</script>

