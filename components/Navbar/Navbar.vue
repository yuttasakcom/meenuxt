<template>
    <div>
        <nav class="teal">
            <div class="nav-wrapper">
                <nuxt-link to="/" class="brand-logo">DevMeetup</nuxt-link>
                
                <a href="#" data-activates="slide-out" class="button-collapse">
                   <i class="material-icons">menu</i>
                </a>

                <ul class="right hide-on-med-and-down">
                    <nuxt-link tag="li" to="/">
                        <a>
                            <i class="material-icons left">supervisor_account</i> View Meetups
                        </a>
                    </nuxt-link>
                </ul>
            </div>
        </nav>

        <SideNav />
    </div>
</template>

<script>
import SideNav from './SideNav'
export default {
  components: {
    SideNav
  }
}
</script>

