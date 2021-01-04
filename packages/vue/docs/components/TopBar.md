# TopBar

Top Bar component with righ or left aligned content.

[[toc]]

## Most common usage scenario

<div class="vuepress-mobile">
    <label for="vuepress-mobile" class="vuepress-mobile-label">Mobile view</label><input id="vuepress-mobile" type="checkbox" class="vuepress-mobile-checkbox">
    <iframe class="storybook-iframe" src="https://storybook.storefrontui.io/iframe.html?id=organisms-topbar--common" style="width: 100%; border: 0; border-bottom: 1px solid #eee;height: 10rem"></iframe>
  </div>

```html
<template>
  <SfTopBar>
    <template #center>
      <div style="display: flex;" class="desktop-only">
        <p
          style="
            margin: 0 var(--spacer-sm) 0 0;
            font-size: var(--font-size--base);
            color: var(--c-link);
          "
        >
          Download our application.
        </p>
        <SfButton style="padding: 0;" class="sf-button--text"
          >Find out more</SfButton
        >
      </div>
      <SfImage
        class="smartphone-only"
        src="/assets/storybook/SfTopBar/logo.svg"
        alt="logo"
      />
    </template>
    <template #left>
      <SfButton style="padding: 0;" class="sf-button--text"
        >Help & FAQs</SfButton
      >
    </template>
    <template #right>
      <SfImage
        style="margin-right: var(--spacer-sm);"
        src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzIiIGhlaWdodD0iMzIiIHZpZXdCb3g9IjAgMCAzMiAzMiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGNpcmNsZSBjeD0iMTYiIGN5PSIxNiIgcj0iMTEiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xOC4wOTYgMTMuMjY4QzE4IDEzLjE2NCAxNy44OCAxMy4wNjQgMTcuNzM2IDEyLjk2OEMxNy41OTIgMTIuODY0IDE3LjQyNCAxMi43NzIgMTcuMjMyIDEyLjY5MkMxNy4wNDggMTIuNjA0IDE2Ljg0OCAxMi41MzYgMTYuNjMyIDEyLjQ4OEMxNi40MTYgMTIuNDMyIDE2LjE4OCAxMi40IDE1Ljk0OCAxMi4zOTJWMTUuMjM2TDE2LjEwNCAxNS4yNzJDMTYuNTQ0IDE1LjM2OCAxNi45NCAxNS40OCAxNy4yOTIgMTUuNjA4QzE3LjY1MiAxNS43MjggMTcuOTU2IDE1Ljg4IDE4LjIwNCAxNi4wNjRDMTguNDYgMTYuMjQ4IDE4LjY1MiAxNi40NzIgMTguNzggMTYuNzM2QzE4LjkxNiAxNyAxOC45ODQgMTcuMzI0IDE4Ljk4NCAxNy43MDhDMTguOTg0IDE4LjEwOCAxOC45MDggMTguNDU2IDE4Ljc1NiAxOC43NTJDMTguNjA0IDE5LjA0OCAxOC4zOTYgMTkuMjkyIDE4LjEzMiAxOS40ODRDMTcuODY4IDE5LjY3NiAxNy41NTIgMTkuODI0IDE3LjE4NCAxOS45MjhDMTYuODI0IDIwLjAyNCAxNi40MzYgMjAuMDc2IDE2LjAyIDIwLjA4NFYyMS4yODRIMTUuNDkyVjIwLjA3MkMxNC4zMjQgMjAgMTMuMyAxOS42MDQgMTIuNDIgMTguODg0TDEyLjkzNiAxNy45NzJDMTMuMDU2IDE4LjA5MiAxMy4yMDQgMTguMjE2IDEzLjM4IDE4LjM0NEMxMy41NTYgMTguNDY0IDEzLjc1NiAxOC41NzYgMTMuOTggMTguNjhDMTQuMjEyIDE4Ljc4NCAxNC40NiAxOC44NzYgMTQuNzI0IDE4Ljk1NkMxNC45ODggMTkuMDI4IDE1LjI2NCAxOS4wNzYgMTUuNTUyIDE5LjFWMTYuMjMyTDE1LjM3MiAxNi4xODRDMTQuOTQgMTYuMDggMTQuNTYgMTUuOTY4IDE0LjIzMiAxNS44NDhDMTMuOTA0IDE1LjcyOCAxMy42MjggMTUuNTg0IDEzLjQwNCAxNS40MTZDMTMuMTg4IDE1LjI0OCAxMy4wMjQgMTUuMDQ0IDEyLjkxMiAxNC44MDRDMTIuOCAxNC41NjQgMTIuNzQ0IDE0LjI3NiAxMi43NDQgMTMuOTRDMTIuNzQ0IDEzLjU1NiAxMi44MTIgMTMuMjE2IDEyLjk0OCAxMi45MkMxMy4wODQgMTIuNjE2IDEzLjI3MiAxMi4zNiAxMy41MTIgMTIuMTUyQzEzLjc2IDExLjkzNiAxNC4wNTIgMTEuNzY4IDE0LjM4OCAxMS42NDhDMTQuNzI0IDExLjUyOCAxNS4wOTIgMTEuNDU2IDE1LjQ5MiAxMS40MzJWMTAuMjJIMTYuMDJWMTEuNDMyQzE2LjU0OCAxMS40NTYgMTcuMDI0IDExLjU1MiAxNy40NDggMTEuNzJDMTcuODggMTEuODg4IDE4LjI2NCAxMi4xMTIgMTguNiAxMi4zOTJMMTguMDk2IDEzLjI2OFpNMTcuODMyIDE3LjgxNkMxNy44MzIgMTcuNjA4IDE3Ljc4OCAxNy40MzIgMTcuNyAxNy4yODhDMTcuNjIgMTcuMTM2IDE3LjUgMTcuMDA0IDE3LjM0IDE2Ljg5MkMxNy4xOCAxNi43NzIgMTYuOTg0IDE2LjY2OCAxNi43NTIgMTYuNThDMTYuNTIgMTYuNDkyIDE2LjI1MiAxNi40MDggMTUuOTQ4IDE2LjMyOFYxOS4xMTJDMTYuNTQ4IDE5LjExMiAxNy4wMTIgMTkuMDA0IDE3LjM0IDE4Ljc4OEMxNy42NjggMTguNTcyIDE3LjgzMiAxOC4yNDggMTcuODMyIDE3LjgxNlpNMTMuODYgMTMuNzcyQzEzLjg2IDEzLjk3MiAxMy44OTIgMTQuMTQ0IDEzLjk1NiAxNC4yODhDMTQuMDI4IDE0LjQzMiAxNC4xMzIgMTQuNTU2IDE0LjI2OCAxNC42NkMxNC40MDQgMTQuNzY0IDE0LjU4IDE0Ljg1NiAxNC43OTYgMTQuOTM2QzE1LjAxMiAxNS4wMDggMTUuMjY0IDE1LjA4IDE1LjU1MiAxNS4xNTJWMTIuMzkyQzE0Ljk2OCAxMi40MjQgMTQuNTQgMTIuNTYgMTQuMjY4IDEyLjhDMTMuOTk2IDEzLjA0IDEzLjg2IDEzLjM2NCAxMy44NiAxMy43NzJaIiBmaWxsPSJibGFjayIvPgo8L3N2Zz4K"
        alt="currency"
      />
      <SfImage
        src="/assets/storybook/SfTopBar/flag.png"
        alt="flag of the USA"
      />
    </template>
  </SfTopBar>
</template>
<script>
import { SfTopBar } from "@storefront-ui/vue";
import { SfButton } from "@storefront-ui/vue";
import { SfImage } from "@storefront-ui/vue";
export default {
  components: {
    SfTopBar,
    SfButton,
    SfImage,
  },
};
</script>
```

## Props

None.

## Slots

- **`left`**
  - _Custom left content_

- **`center`**
  - _Custom center content_

- **`right`**
  - _Custom right content_

## Events

None.

## CSS modifiers

None.

## CSS custom properties (variables)

- **`--top-bar-background`**
- **`--top-bar-padding`**
- **`--top-bar-height`**
### Overridden other components CSS variables 
None. 


You can override CSS variables values bound to this component.

<!-- No _internal components -->

## Play with this component

See all available configurations and play with this component on <a href="https://storybook.storefrontui.io/?path=/story/organisms-topbar--common">Storybook</a>.