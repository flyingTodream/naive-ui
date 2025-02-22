# Ellipsis with tooltip

Set `column.ellipsis.tooltip` to make ellipsis have tooltip. `column.ellipsis` accepts the same props as `n-ellipsis`.

```html
<n-data-table :columns="columns" :data="data" :pagination="pagination" />
```

```js
import { defineComponent } from 'vue'

const columns = [
  {
    title: 'Name',
    key: 'name'
  },
  {
    title: 'Age',
    key: 'age'
  },
  {
    title: 'Address',
    key: 'address',
    width: 100,
    ellipsis: {
      tooltip: true
    }
  },
  {
    title: 'Another Address',
    key: 'anotherAddress',
    width: 100,
    ellipsis: {
      tooltip: true
    }
  }
]

const data = [
  {
    key: 0,
    name: 'John Brown',
    age: 32,
    address: 'New York No. 1 Lake Park',
    anotherAddress: 'New York No. 1 Lake Park'
  },
  {
    key: 1,
    name: 'Jim Green',
    age: 42,
    address: 'London No. 1 Lake Park',
    anotherAddress: 'New York No. 1 Lake Park'
  },
  {
    key: 2,
    name: 'Joe Black',
    age: 32,
    address: 'Sidney No. 1 Lake Park',
    anotherAddress: 'New York No. 1 Lake Park'
  }
]

export default defineComponent({
  setup () {
    return {
      data,
      columns,
      pagination: { pageSize: 10 }
    }
  }
})
```
