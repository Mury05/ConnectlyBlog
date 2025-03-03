<script lang="ts" setup>
const links = [
    {
        label: 'Ressources',
        children: [
            { label: 'Starter Kits' },
            { label: 'Release Notes' },
            { label: 'Blog', },
            { label: 'Partners', },
            { label: 'News', },
            { label: 'Jobs', },
            { label: 'Careers', },
        ],
    },
    {
        label: 'Products',
        children: [
            { label: 'Cloud' },
            { label: 'Forge' },
            { label: 'Nightwatch' },
            { label: 'Nova' },
        ]
    },
    {
        label: 'Packages',
        children: [
            { label: 'Cashier' },
            { label: 'Dusk' },
            { label: 'Horizon' },
            { label: 'Octane' },
            { label: 'Scout' },
            { label: 'Pennant' },
            { label: 'Pint' },
        ],
    }
];
</script>


<template>
    <UFooter>
        <template #top>
            <UContainer>
                <UFooterColumns :links="links">
                    <template #right>
                        <UFormField name="email" label="S'inscrire à notre newsletter">
                            <UInput placeholder="Entrer votre email">
                                <template #trailing>
                                    <UButton type="submit" size="xs" label="S'inscrire" color="orange" />
                                </template>
                            </UInput>
                        </UFormField>
                    </template>
                </UFooterColumns>
            </UContainer>
        </template>
        <template #left>
            <p class="text-sm">Copyright &copy; {{ new Date().getFullYear() }}. Tous droits réservés.</p>
        </template>
        <template #right>
            <UColorModeButton />
        </template>
        <template #center>
            <UButton color="white" to="https://github.com/Mury05/connectly" target="_blank" icon="devicon:githubcodespaces"/>
            <!-- <UFooterSocialLinks /> -->
        </template>
    </UFooter>
</template>


<style scoped></style>