# adapt-pageHeader

**pageHeader** is a *presentation component* that can be used at the top of a page to provide page header functionality (text and image or background image).

### When to use
Use **pageHeader** in place of the built-in theme page header functionality for both the Framework and the Authoring Tool. Use with the built-in v5 theme class `hide-page-header`. The use of the **pageHeader** component does not impact the menu header, which must be defined by the menu plugin itself.

### What's included
The component comes with four predefined configuration options for the page header. They are:

* Image (within content width) with text overlaid
* Image (within content width) with text below
* Image (outside of content width) with text overlaid
* Image (outside of content width) with text below

## Settings Overview

The attributes listed below are used in *components.json* to configure **pageHeader**, and are properly formatted as JSON in [*example.json*](https://github.com/cgkineo/adapt-pageHeader/blob/master/example.json).

### Attributes

[**core model attributes**](https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes): These are inherited by every Adapt component. [Read more](https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes).

**\_component** (string): This value must be: `pageHeader`. (One word.)

**\_classes** (string): CSS class name to be applied to **PageHeader**’s containing `div`. The class must be predefined in one of the Less files (see below). Separate multiple classes with a space.

**\_layout** (string): This defines the horizontal position of the component in the block. Acceptable values are `full`, `left` or `right`. It is recommended that this be set to `full`.

**instruction** (string): This optional text is frequently used to guide the learner’s interaction with the component.

**\_extendComponentContainer** (boolean): When true, removes the max width of the parent block and expands the component to fill the entire width of the block. When false, inherits the default block max width. Default is `true`.

**\_hasTextBelowImage** (boolean): When true, image appears in an `img` element above the `pageHeader` text. When false, image is set as a background-image on the component container element. Default is `false`.

**\_images** (object): The image that acts as either background to component or an image above text. It contains values for **alt**, **large**, **medium** and **small**.

>**\_large** (string): File name (including path) of the image used with large device width. Path should be relative to the *src* folder (e.g., *course/en/images/origami-menu-two.jpg*).

>**\_medium** (string): File name (including path) of the image used with medium device width. Path should be relative to the *src* folder (e.g., *course/en/images/origami-menu-two.jpg*).

>**\_small** (string): File name (including path) of the image used with small device width. Path should be relative to the *src* folder (e.g., *course/en/images/origami-menu-two.jpg*).

>**alt** (string): This text becomes the image’s `alt` attribute. Only used when `"_hasTextBelowImage": true`.

**_backgroundStyles** (object): Additional attributes available to customise how background images display. **Only used when `"_hasTextBelowImage": false`.** The backgroundStyles object contains values for **\_backgroundRepeat**, **\_backgroundSize** and **\_backgroundPosition**.

>**\_backgroundRepeat** (string): This attribute defines how the background image repeats. Properties include **repeat**, **repeat-x**, **repeat-y** and **no-repeat**. Repeat-x: The background image is repeated only horizontally. Repeat-y: The background image is repeated only vertically.

>**\_backgroundSize** (string): This attribute defines the size the background image display. Properties include **auto**, **cover** and **contain**. Auto: The background image is displayed in its original size. Cover: Resize the background image to cover the entire container, even if it has to stretch or crop the image. Contain: Resize the background image to make sure the image is fully visible.

**\_minimumHeights** (object): The minimum heights attribute group specifies the minimum height of the image container at different device widths (`_large`, `_medium`, and `_small`). **Only used when `"_hasTextBelowImage": false`.**

>**\_large** (number): The minimum height should only be used in instances where the image container height needs to be greater than the content e.g. to prevent a background image being cropped.

>**\_medium** (number): The minimum height should only be used in instances where the image container height needs to be greater than the content e.g. to prevent a background image being cropped.

>**\_small** (number): The minimum height should only be used in instances where the image container height needs to be greater than the content e.g. to prevent a background image being cropped.

### Pre-defined classes

**text-align-vert-center**: Vertically aligns component to center in component container. **Only used when `"_hasTextBelowImage": false`.**

**text-align-vert-bottom**: Vertically aligns component to bottom in component container. **Only used when `"_hasTextBelowImage": false`.**

----------------------------
**Version number:**  1.0.0<br/>
**Framework versions:**  5.3+<br/>
**Vanilla versions:**  5.2+<br/>
**Author / maintainer:**  Kineo<br/>
**Accessibility support:**  WAI AA<br/>
**RTL support:**  Yes<br/>
**Cross-platform coverage:** Chrome, Chrome for Android, Firefox (ESR + latest version), Edge, IE11, Safari 12+13 for macOS/iOS/iPadOS, Opera<br/>
