---
badges:
  - removed
---

# $children <MigrationBadges :badges="$frontmatter.badges" />

## Overview

The `$children` instance property has been removed from Leaf 3.0 and is no longer supported.

## 2.x Syntax

In 2.x, developers could access direct child components of the current instance with `this.$children`:

```Leaf
<template>
  <div>
    <img alt="Leaf logo" src="./assets/logo.png">
    <my-button>Change logo</my-button>
  </div>
</template>

<script>
import MyButton from './MyButton'

export default {
  components: {
    MyButton
  },
  mounted() {
    console.log(this.$children) // [LeafComponent]
  }
}
</script>
```

## 3.x Update

In 3.x, the `$children` property is removed and no longer supported. Instead, if you need to access a child component instance, we recommend using [$refs](/v3.x/docs/component-template-refs.html#template-refs).

## Migration Strategy

[Migration build flag: `INSTANCE_CHILDREN`](migration-build.html#compat-configuration)