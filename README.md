# React Native Gifted Table

The 0 dependency HTML-like approach to bring tables to React Native that do not rely on flex or hard-coded columns width.

## Installation

```
yarn add react-native-gifted-table
```

or

```
npm install react-native-gifted-table
```

## Usage

```jsx
import React from 'react'
import { Text } from 'react-native'
import { Table, Row, Cell } from 'react-native-gifted-table'

const MyComponent = () => (
  <Table>
    <Row>
      <Cell render={() => <Text>Alice</Text>}/>
      <Cell render={() => <Text>Bob</Text>}/>
      <Cell render={() => <Text>Claire</Text>}/>
    </Row>
    <Row>
      <Cell render={() => <Text>15 points</Text>}/>
      <Cell render={() => <Text>12 points</Text>}/>
      <Cell render={() => <Text>Did not play</Text>}/>
    </Row>
  </Table>
)
```

> For large tables, you may want to wrap your table in scrollable components.

## Styling

No cosmetic styling is made by the library other than setting the width on the cells. It's up to you to provide `style` props to any of the `<Table />`, `<Row />` or `<Cell />` components if you want to customize your tables. There's no restrictions as to what styling properties you may use to the exception of `width` on `<Cell />`.

The library adjusts each `<Cell />`'s width to the largest cell in the column.

:warning: It is important that all of your rows contain the same number of cells. If you want to "skip" a cell, simply add an empty `<Cell />` as a placeholder. There is currently no way to have a cell span over multiple columns.



