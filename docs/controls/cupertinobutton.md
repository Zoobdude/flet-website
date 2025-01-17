---
title: CupertinoButton
sidebar_label: CupertinoButton
slug: cupertinobutton
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

An iOS-style button.

## Examples

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinobutton)

### Basic Example

<Tabs groupId="language">
  <TabItem value="python" label="Python" default>

```python
import flet as ft

def main(page: ft.Page):
    page.add(
        ft.CupertinoButton(
            content=ft.Text("Normal CupertinoButton", color=ft.cupertino_colors.DESTRUCTIVE_RED),
            opacity_on_click=0.3,
            on_click=lambda e: print("Normal CupertinoButton clicked!"),
        ),
        ft.CupertinoButton(
            content=ft.Text("Filled CupertinoButton", color=ft.colors.YELLOW),
            filled=True,
            alignment=ft.alignment.top_left,
            border_radius=ft.border_radius.all(15),
            opacity_on_click=0.5,
            on_click=lambda e: print("Filled CupertinoButton clicked!"),
        ),
        ft.ElevatedButton(
            adaptive=True,  # a CupertinoButton will be rendered when running on apple-platform
            bgcolor=ft.cupertino_colors.SYSTEM_TEAL,
            content=ft.Row(
                [
                    ft.Icon(name=ft.icons.FAVORITE, color="pink"),
                    ft.Text("ElevatedButton+adaptive"),
                ],
                tight=True,
            ),
        ),
    )


ft.app(target=main)
```
  </TabItem>

</Tabs>

<img src="/img/docs/controls/cupertino-button/basic-cupertino-buttons.png" className="screenshot-20" />

## Properties

### `bgcolor`

Button's background [color](/docs/guides/python/colors).

### `disabled_color`

The background [color](/docs/guides/python/colors) of the button when it is disabled.

### `content`

A Control representing custom button content.

### `elevation`

Button's elevation.

### `filled`

Whether the button has a filled background or not. Defaults to `False`.

### `icon`

Icon shown in the button.

### `icon_color`

Icon [color](/docs/guides/python/colors).

### `min_size`

The minimum size of the button. Defaults to `44.0`.

### `opacity_on_click`

Defines the opacity of the button when it is clicked. Defaults to `0.4`. The button will have an opacity of `1.0` when it is not pressed.

### `padding`

The amount of space to surround the `content` control inside the bounds of the button.

### `text`

The text displayed on a button.

### `tooltip`

The text displayed when hovering the mouse over the button.

### `url`

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`

Where to open URL in the web mode:

* `_blank` (default) - new tab/window.
* `_self` - the current tab/window.

## Events

### `on_click`

Fires when a user clicks the button.
