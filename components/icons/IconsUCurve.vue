<script setup>
const theme = useTheme()
</script>
<template>
    <svg class="min-w-full" viewBox="0 0 1440 270" fill="none" xmlns="http://www.w3.org/2000/svg">
        <g filter="url(#filter0_b_448_678)">
            <path d="M699 148L1440 0V270H0V174C77 302 513 188 699 148Z" :fill="theme ? '#1A1C22' : '#F5F5F5'"
                :fill-opacity="theme ? '0.4' : '0.4'" />
        </g>
        <g filter="url(#filter1_b_448_678)">
            <path d="M695 160L1440 20V270H0V174C77 302 509 200 695 160Z" :fill="theme ? '#1A1C22' : '#F5F5F5'"
                :fill-opacity="theme ? '0.5' : '0.5'" />
        </g>
        <g filter="url(#filter2_b_448_678)">
            <path d="M709 174L1440 42V270H0V174C77 302 523 214 709 174Z" :fill="theme ? '#1A1C22' : '#F5F5F5'"
                :fill-opacity="theme ? '0.7' : '0.6'" />
        </g>
        <defs>
            <filter id="filter0_b_448_678" x="-4" y="-4" width="1448" height="278" filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB">
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feGaussianBlur in="BackgroundImage" stdDeviation="2" />
                <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_448_678" />
                <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_448_678" result="shape" />
            </filter>
            <filter id="filter1_b_448_678" x="-4" y="16" width="1448" height="258" filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB">
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feGaussianBlur in="BackgroundImage" stdDeviation="2" />
                <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_448_678" />
                <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_448_678" result="shape" />
            </filter>
            <filter id="filter2_b_448_678" x="-4" y="38" width="1448" height="236" filterUnits="userSpaceOnUse"
                color-interpolation-filters="sRGB">
                <feFlood flood-opacity="0" result="BackgroundImageFix" />
                <feGaussianBlur in="BackgroundImage" stdDeviation="2" />
                <feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_448_678" />
                <feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_448_678" result="shape" />
            </filter>
        </defs>
    </svg>
</template>