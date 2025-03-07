---
id: "components.SimpleClipper"
title: "Class: SimpleClipper<Plane>"
sidebar_label: "SimpleClipper"
custom_edit_url: null
---

[components](../modules/components.md).SimpleClipper

A lightweight component to easily create and handle
[clipping planes](https://threejs.org/docs/#api/en/materials/Material.clippingPlanes).

**`Param`**

the instance of [Components](components.Components.md) used.

**`Param`**

the type of plane to be used by the clipper.
E.g. [SimplePlane](components.SimplePlane.md).

## Type parameters

| Name | Type |
| :------ | :------ |
| `Plane` | extends [`SimplePlane`](components.SimplePlane.md) |

## Hierarchy

- [`Component`](components.Component.md)<`Plane`[]\>

  ↳ **`SimpleClipper`**

  ↳↳ [`EdgesClipper`](components.EdgesClipper.md)

## Implements

- [`Createable`](../interfaces/components.Createable.md)
- [`Disposable`](../interfaces/components.Disposable.md)
- [`Hideable`](../interfaces/components.Hideable.md)
- [`UI`](../interfaces/components.UI.md)

## Properties

### afterCreate

• **afterCreate**: [`Event`](components.Event.md)<`Plane`\>

[afterCreate](../interfaces/components.Createable.md#aftercreate)

#### Implementation of

[Createable](../interfaces/components.Createable.md).[afterCreate](../interfaces/components.Createable.md#aftercreate)

#### Defined in

temp/components/core/SimpleClipper/index.ts:34

___

### afterDelete

• **afterDelete**: [`Event`](components.Event.md)<`Plane`\>

[afterDelete](../interfaces/components.Createable.md#afterdelete)

#### Implementation of

[Createable](../interfaces/components.Createable.md).[afterDelete](../interfaces/components.Createable.md#afterdelete)

#### Defined in

temp/components/core/SimpleClipper/index.ts:37

___

### afterDrag

• **afterDrag**: [`Event`](components.Event.md)<`void`\>

Event that fires when the user stops dragging a clipping plane.

#### Defined in

temp/components/core/SimpleClipper/index.ts:66

___

### beforeDrag

• **beforeDrag**: [`Event`](components.Event.md)<`void`\>

Event that fires when the user starts dragging a clipping plane.

#### Defined in

temp/components/core/SimpleClipper/index.ts:63

___

### name

• **name**: `string` = `"SimpleClipper"`

[name](components.Component.md#name)

#### Overrides

[Component](components.Component.md).[name](components.Component.md#name)

#### Defined in

temp/components/core/SimpleClipper/index.ts:31

___

### orthogonalY

• **orthogonalY**: `boolean` = `false`

Whether to force the clipping plane to be orthogonal in the Y direction
(up). This is desirable when clipping a building horizontally and a
clipping plane is created in it's roof, which might have a slight
slope for draining purposes.

#### Defined in

temp/components/core/SimpleClipper/index.ts:53

___

### toleranceOrthogonalY

• **toleranceOrthogonalY**: `number` = `0.7`

The tolerance that determines whether a horizontallish clipping plane
will be forced to be orthogonal to the Y direction. [orthogonalY](components.SimpleClipper.md#orthogonaly)
has to be `true` for this to apply.

#### Defined in

temp/components/core/SimpleClipper/index.ts:60

## Accessors

### enabled

• `get` **enabled**(): `boolean`

[enabled](components.Component.md#enabled)

#### Returns

`boolean`

#### Overrides

Component.enabled

#### Defined in

temp/components/core/SimpleClipper/index.ts:75

• `set` **enabled**(`state`): `void`

[enabled](components.Component.md#enabled)

#### Parameters

| Name | Type |
| :------ | :------ |
| `state` | `boolean` |

#### Returns

`void`

#### Overrides

Component.enabled

#### Defined in

temp/components/core/SimpleClipper/index.ts:80

___

### material

• `get` **material**(): `Material`

The material of the clipping plane representation.

#### Returns

`Material`

#### Defined in

temp/components/core/SimpleClipper/index.ts:103

• `set` **material**(`material`): `void`

The material of the clipping plane representation.

#### Parameters

| Name | Type |
| :------ | :------ |
| `material` | `Material` |

#### Returns

`void`

#### Defined in

temp/components/core/SimpleClipper/index.ts:108

___

### size

• `get` **size**(): `number`

The size of the geometric representation of the clippings planes.

#### Returns

`number`

#### Defined in

temp/components/core/SimpleClipper/index.ts:116

• `set` **size**(`size`): `void`

The size of the geometric representation of the clippings planes.

#### Parameters

| Name | Type |
| :------ | :------ |
| `size` | `number` |

#### Returns

`void`

#### Defined in

temp/components/core/SimpleClipper/index.ts:121

___

### visible

• `get` **visible**(): `boolean`

[visible](../interfaces/components.Hideable.md#visible)

#### Returns

`boolean`

#### Implementation of

[Hideable](../interfaces/components.Hideable.md).[visible](../interfaces/components.Hideable.md#visible)

#### Defined in

temp/components/core/SimpleClipper/index.ts:90

• `set` **visible**(`state`): `void`

[visible](../interfaces/components.Hideable.md#visible)

#### Parameters

| Name | Type |
| :------ | :------ |
| `state` | `boolean` |

#### Returns

`void`

#### Implementation of

[Hideable](../interfaces/components.Hideable.md).[visible](../interfaces/components.Hideable.md#visible)

#### Defined in

temp/components/core/SimpleClipper/index.ts:95

## Methods

### create

▸ **create**(): `void`

[create](../interfaces/components.Createable.md#create)

#### Returns

`void`

#### Implementation of

Createable.create

#### Defined in

temp/components/core/SimpleClipper/index.ts:163

___

### createFromNormalAndCoplanarPoint

▸ **createFromNormalAndCoplanarPoint**(`normal`, `point`): `Plane`

Creates a plane in a certain place and with a certain orientation,
without the need of the mouse.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `normal` | `Vector3` | the orientation of the clipping plane. |
| `point` | `Vector3` | the position of the clipping plane. |

#### Returns

`Plane`

#### Defined in

temp/components/core/SimpleClipper/index.ts:179

___

### delete

▸ **delete**(`plane?`): `void`

[delete](../interfaces/components.Createable.md#delete)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `plane?` | `Plane` | the plane to delete. If undefined, the the first plane found under the cursor will be deleted. |

#### Returns

`void`

#### Implementation of

Createable.delete

#### Defined in

temp/components/core/SimpleClipper/index.ts:194

___

### deleteAll

▸ **deleteAll**(): `void`

Deletes all the existing clipping planes.

#### Returns

`void`

#### Defined in

temp/components/core/SimpleClipper/index.ts:202

___

### dispose

▸ **dispose**(): `void`

[get](components.Component.md#get)

#### Returns

`void`

#### Implementation of

Disposable.dispose

#### Defined in

temp/components/core/SimpleClipper/index.ts:151

___

### get

▸ **get**(): `Plane`[]

[get](components.Component.md#get)

#### Returns

`Plane`[]

#### Overrides

[Component](components.Component.md).[get](components.Component.md#get)

#### Defined in

temp/components/core/SimpleClipper/index.ts:146

___

### hasUI

▸ **hasUI**(): this is UI

Whether is component implements any kind of [UI](../interfaces/components.UI.md).

#### Returns

this is UI

#### Inherited from

[Component](components.Component.md).[hasUI](components.Component.md#hasui)

#### Defined in

temp/components/base-types/component.ts:48

___

### isDisposeable

▸ **isDisposeable**(): this is Disposable

Whether is component is [Disposable](../interfaces/components.Disposable.md).

#### Returns

this is Disposable

#### Inherited from

[Component](components.Component.md).[isDisposeable](components.Component.md#isdisposeable)

#### Defined in

temp/components/base-types/component.ts:28

___

### isHideable

▸ **isHideable**(): this is Hideable

Whether is component is [Hideable](../interfaces/components.Hideable.md).

#### Returns

this is Hideable

#### Inherited from

[Component](components.Component.md).[isHideable](components.Component.md#ishideable)

#### Defined in

temp/components/base-types/component.ts:43

___

### isResizeable

▸ **isResizeable**(): this is Resizeable

Whether is component is [Resizeable](../interfaces/components.Resizeable.md).

#### Returns

this is Resizeable

#### Inherited from

[Component](components.Component.md).[isResizeable](components.Component.md#isresizeable)

#### Defined in

temp/components/base-types/component.ts:33

___

### isUpdateable

▸ **isUpdateable**(): this is Updateable

Whether is component is [Updateable](../interfaces/components.Updateable.md).

#### Returns

this is Updateable

#### Inherited from

[Component](components.Component.md).[isUpdateable](components.Component.md#isupdateable)

#### Defined in

temp/components/base-types/component.ts:38
