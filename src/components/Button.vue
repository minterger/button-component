<template>
  <button :class="[variantClass, shadowClass, colorClass, sizeClass, activeClass]">
    <span v-if="startIcon" class="startIcon material-icons">{{startIcon}}</span>
    <slot/>
    <span v-if="endIcon" class="endIcon material-icons">{{endIcon}}</span>
  </button>
</template>

<script>
export default {
  data() {
    return {
      textButton: '',
    }
  },
  props: {
    variant: String,
    disableShadow: Boolean,
    active: Boolean,
    color: String,
    size: String,
    startIcon: String,
    endIcon: String
  },
  computed: {
    variantClass() {
      if (this.variant == 'text') return 'text'
      if (this.variant == 'outline') return 'outline'
      return 'button'
    },
    shadowClass() {
      if (this.disableShadow) return ''
      return 'shadow'
    },
    activeClass() {
      if (this.active) return 'active'
      return ''
    },
    colorClass() {
      if (this.color == 'danger') return 'danger'
      if (this.color == 'primary') return 'primary'
      if (this.color == 'secondary') return 'secondary'
      return 'default'
    },
    sizeClass() {
      if (this.size == 'lg') return 'lg'
      if (this.size == 'md') return 'md'
      return 'sm'
    }
  }
}
</script>

<style scoped>

/*variables color button normal*/
.button.default {
  --color: #3F3F3F;
  --background: #E0E0E0;
  --hover-background: #AEAEAE;
}
.button.primary {
  --color: #FFFFFF;
  --background: #2962FF;
  --hover-background: #0039CB;
}
.button.secondary {
  --color: #FFFFFF;
  --background: #455A64;
  --hover-background: #1C313A;
}
.button.danger {
  --color: #FFFFFF;
  --background: #D32F2F;
  --hover-background: #9A0007;
}

  /*variables outline and text colors*/
.outline.default, .text.default, .outline.primary, .text.primary{
  --color: #3D5AFE;
  --color-hover: #EAF0FF;
}
.outline.danger, .text.danger {
  --color: #D32F2F;
  --color-hover: #ffeaea;
}
.outline.secondary, .text.secondary {
  --color: #455A64;
  --color-hover: #edf6fc;
}

/*boton*/
button {
  margin: 5px 5px;
  cursor: pointer;
  font-weight: 600;
  border-radius: 7px;
  border: none;
  transition: background .2s;
}

/*Tamaños*/
.sm {
  padding: 8px 13px;
}
.md {
  padding: 11px 18px;
}
.lg {
  padding: 13px 25px;
}

/*boton por defecto*/
.button {
  background: var(--background);
  color: var(--color);
}
.button:hover, .button:focus, .button.active {
  background: var(--hover-background);
}

/*Outline button*/
.outline {
  color: var(--color);
  border: 1px solid var(--color);
  background: #f5f5f5;
}
.outline:hover, .outline:focus, .outline.active {
  background: var(--color-hover);
}

/*text button*/
.text {
  color: var(--color);
  background: #f5f5f5;
}
.text:hover, .text:focus, .text.active {
  background: var(--color-hover);
}

/*button shadow*/
.shadow {
  box-shadow: 2px 2px 5px #c9c9c9;
}

/*icon*/
.material-icons {
  font-size: 10px;
  transform:scale(1.6);
}

.startIcon {
  padding: 0 8px 0 3px;
}

.endIcon {
  padding: 0 3px 0 8px;
}
</style>