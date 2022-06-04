<template>
    <ul class="blockchain-picker no-markers">
        <li>
            <label for="bc-opera">
                <input
                    id="bc-opera"
                    v-model="blockchain"
                    type="radio"
                    name="blockchain"
                    value="opera"
                    class="not-visible"
                />
                <span>
                    <icon
                        data="@/assets/svg/chain-logos/fantom-active.svg"
                        width="64"
                        height="64"
                        original
                        aria-hidden="true"
                        class="logo-active"
                    />
                    <icon
                        data="@/assets/svg/chain-logos/fantom-inactive.svg"
                        width="64"
                        height="64"
                        original
                        aria-hidden="true"
                        class="logo-inactive"
                    />
                    <span class="title">Fantom Opera</span>
                </span>
            </label>
        </li>
    </ul>
</template>

<script>
import appConfig from '../../../app.config.js';

export default {
    name: 'BlockchainPicker',

    props: {
        disableETH: {
            type: Boolean,
            default: false,
        },
        disableBNB: {
            type: Boolean,
            default: false,
        },
    },

    data() {
        return {
            blockchain: 'opera',
            appConfig,
        };
    },

    watch: {
        blockchain(_value) {
            this.$emit('blockchain-pick', _value);
        },
    },
};
</script>

<style lang="scss">
@import 'style';
</style>
