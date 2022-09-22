<template>
    <div class="settingslinks">
        <f-card class="f-card-double-padding">
            <div class="small-container">
                <p>
                    <a href="https://www.instagram.com/testing/" rel="noopener" target="_blank">
                        How to use GO fWallet
                    </a>
                </p>

                <p>
                    <a href="https://explorer.fantom.network/" rel="noopener" target="_blank">Explorer </a>
                </p>

                <social-media-links />
            </div>
        </f-card>
    </div>
</template>

<script>
import SocialMediaLinks from '@/components/SocialMediaLinks/SocialMediaLinks.vue';
import FCard from '@/components/core/FCard/FCard.vue';

export default {
    name: 'SettingsLinks',

    components: { FCard, SocialMediaLinks },
};
</script>
