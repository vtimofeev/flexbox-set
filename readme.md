# Flexbox styles set.
This is a set of css classes to create layout with flexbox.


## Use with npm and webpack

Install package
`
npm install flexbox-set
`

Import in JS file (webpack)
`
import 'flexbox-set/src/index.css'
`

Usage
```
<div class="flex-columns flex--main-center flex--cross-center">
    <div class="flex-cell">50%</div>
    <div class="flex-cell">50%</div>
</div>

<div class="flex-columns flex--main-center flex--cross-center">
    <div class="flex-cell--1-3">1/3</div>
    <div class="flex-cell--2-3">2/3</div>
</div>
```

## Containers classes

#### `flex-columns` or `flex`
Sets container display:flex and flex-direction:row (from left to right).

#### `flex-rows`
Sets container display:flex and direction:column (from top to bottom).

## Containers settings

Settings of container starts from `flex--`

### Items alignment in main axis (from left to right when `flex-columns` is used)

**flex--main-start** (default)

Sets justify-content:flex-start.
If container is `flex-columns` then flex-items starts from left to right.


**flex--main-end**

Sets justify-content:flex-end.
If container is `flex-columns` then flex-items starts from right to left.

**flex--main-center**
Sets justify-content:center.
Items align by center main axis (left to right line if `flex-columns`)

**flex--main-around**

Sets justify-content:space-around.
Items will be distributed evenly. They have empty spaces at the start and end.

**flex--main-between**

Sets justify-content:space-between.
Items will be distributed evenly. They have no empty spaces at the start and end.

### Items alignment in cross axis (from top to bottom when `flex-columns` is used)

**flex--cross-start**

Sets align-items:flex-start.

**flex--cross-end**

Sets align-items:flex-end.

**flex--cross-center**

Sets align-items:flex-center.

**flex--cross-stretch** (default)

Sets align-items:stretch.

### Item content alignment in cross axis when has multiple columns `flex-wrap:wrap` (from top to bottom when `flex-columns` is used)

**flex-multi--cross-start**

**flex-multi--cross-end**

**flex-multi--cross-center**

**flex-multi--cross-around**

**flex-multi--cross-between**

**flex-multi--cross-stretch** (default)

## Items classes

#### flex-cell

Item will fill all free space in the main axis.

Sets flex item parameters grow 1 and shrink 1;
Flex basis is auto.

#### flex-cell--static

Item size will be as the content size in the main axis.

Sets flex item parameters grow 0 and shrink 0;
Flex basis is auto.

#### flex-cell--full
Set flex basis 100%, for example:
If container is `flex-columns` item will be width 100%
if container is `flex-rows` item will be height 100%

#### flex-cell--1-2
Set flex basis 50%

#### flex-cell--1-3
Set flex basis 33%

#### flex-cell--2-3
Set flex basis 66%

#### flex-cell--1-4
Set flex basis 25%

#### flex-cell--1-5
Set flex basis 20%
