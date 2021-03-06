[◄ Back to index](index.md)
# ![Panel icon](assets/panel-32x32.png) Joomla\Content\Element\Panel

A panel is a particular arrangement of information grouped together for presentation to users in a window or pop-up.

_From [Wikipedia](https://en.wikipedia.org/wiki/Panel_(computer_software))_

Panels are used to add a title to a group of elements for use in collections, like [Accordion](Accordion.md) or
[Tabs](Tabs.md).

## Usage

```php
$panelElement = new Panel( ContentElementInterface[] $elements, string $title [, array $params ] );
```

or

```php
$panelElement = Panel::from( ContentElementInterface $data [, array $mapping [, array $params ] ] );
```

`data` or `params` must contain values for the required constructor argument `title`.

## Properties

Property | Type   | Description  | Required
-------- | ------ | ------------ | ----
elements | ContentElementInterface[] | The child elements | yes
title | string | The title for the panel. | yes

#### Elements

Get the child elements.



```php
$elements = $panelElement->getElements();
```

#### Title

Get the title for the panel.



```php
$title = $panelElement->get( 'title' );
```

## Parameters

Parameters are optional settings for the presentation.
All elements can have 'id' and 'class' parameters; other depend on environment 
and/or renderer.

Parameter | Type   | Description
--------- | ------ | -----------
id        | string | The ID of the element
class     | string | CSS class

#### Parameter List

Get an associative array with all parameters.

```php
$params = $panelElement->getParameters();
```

#### Single Parameter

Retrieve a single parameter. Default should be provided.

```php
$id    = $panelElement->getParameter( 'id' [, $default ] );
$class = $panelElement->getParameter( 'class' [, $default ] );
```

## Examples

