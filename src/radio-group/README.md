# Visual Studio Code Radio Group

The `vscode-radio-group` is a web component implementation of a [radio group](https://w3c.github.io/aria-practices/#radiobutton).

![Radio group hero](/docs/assets/images/radio-group-hero.png)

## Usage

| ❌ Don't                                                                                                                 | ✅ Do                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| ![Radio buttons that indicate multiple options can be selected](/docs/assets/images/radio-dont-1.png)                    | ![Radio buttons with one clear possible selection](/docs/assets/images/radio-do-1.png) |
| Don't use radio buttons when more than one selection is possible. Try using [checkboxes](../checkbox/README.md) instead. | Use radio groups for options that feature a single selection at a time.                |

| ❌ Don't                                                                                    | ✅ Do                                                                                   |
| ------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| ![Radio buttons arranged in a horizontal orientation](/docs/assets/images/radio-dont-2.png) | ![Radio buttons arranged in a vertical orientation](/docs/assets/images/radio-do-2.png) |
| Avoid using horizontal radio group layouts.                                                 | Arrange radio groups vertically to make it easy to scan and compare options.            |

| ❌ Don't                                                                    | ✅ Do                                                                    |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| ![Radio options with multi-line text](/docs/assets/images/radio-dont-3.png) | ![Radio buttons with concise labels](/docs/assets/images/radio-do-3.png) |
| Don't use long blocks of text.                                              | Use concise language to describe each option.                            |

## Implementation

While any DOM content is permissible as a child of the `vscode-radio-group`, only `vscode-radio` components and slotted content with a role of `radio` will receive keyboard support.

## Attributes

| Attribute     | Type    | Description                                                                                  |
| ------------- | ------- | -------------------------------------------------------------------------------------------- |
| `disabled`    | boolean | Disables the radio group and child radios.                                                   |
| `name`        | string  | The name of the radio group. This will also set the name value for all child radio elements. |
| `orientation` | string  | The orientation of the group. Options: `horiztonal`, `vertical`.                             |
| `readonly`    | boolean | When true, the child radios will be immutable by user interaction.                           |

### Basic Radio Group

[Interactive Storybook Example](https://microsoft.github.io/vscode-webview-ui-toolkit/?path=/story/library-radio-group--default)

```html
<vscode-radio-group>
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>
```

### Disabled Attribute

[Interactive Storybook Example](https://microsoft.github.io/vscode-webview-ui-toolkit/?path=/story/library-radio-group--with-disabled)

```html
<vscode-radio-group disabled>
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>
```

### Name Attribute

```html
<vscode-radio-group name="example-radio-group">
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>
```

### Orientation Attribute

If the orientation attribute is not set, the default orientation is `horizontal`.

[Interactive Storybook Example](https://microsoft.github.io/vscode-webview-ui-toolkit/?path=/story/library-radio-group--with-vertical-orientation)

```html
<vscode-radio-group orientation="vertical">
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>

<vscode-radio-group orientation="horizontal">
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>
```

### Read Only Attribute

[Interactive Storybook Example](https://microsoft.github.io/vscode-webview-ui-toolkit/?path=/story/library-radio-group--with-read-only)

```html
<vscode-radio-group readonly>
  <label slot="label">Radio Group Label</label>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
  <vscode-radio>Radio Label</vscode-radio>
</vscode-radio-group>
```
