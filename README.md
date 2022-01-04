# react-native-select

Dropdown package for react-native

## Installation

```sh
npm install react-native-select
```

## Usage

```js
import * as React from 'react';

import { StyleSheet, View } from 'react-native';
import DropdownSelect from 'react-native-select';

export default function App() {
  const [result, setResult] = React.useState<number | undefined>();

  return (
      <DropdownSelect
        label="Country"
        placeholder="Select an option..."
        options={[
          { name: 'Albania', code: 'AL' },
          { name: 'Åland Islands', code: 'AX' },
          { name: 'Algeria', code: 'DZ' },
          { name: 'American Samoa', code: 'AS' },
          { name: 'Andorra', code: 'AD' },
          { name: 'Angola', code: 'AO' },
          { name: 'Anguilla', code: 'AI' },
          { name: 'Antarctica', code: 'AQ' },
          { name: 'Antigua and Barbuda', code: 'AG' },
        ]}
        optionLabel={'name'}
        optionValue={'code'}
        selectedValue={result}
        onValueChange={(itemValue) => setResult(itemValue)}
      />
  );
}
```

| Proptypes              | Datatype            | Example                                          |
| ---------------------- | ------------------- | ------------------------------------------------ |
| label                  | `string`            | `Countries`                                      |
| placeholder            | `string`            | `Select a country`                               |
| options                | `Array`             | `[{ name: 'Albania', code: 'AL' }, { name: 'Åland Islands', code: 'AX' }]` |
| optionLabel            | `string`            | `name`                                           |
| optionValue            | `string`            | `code`                                           |
| selectedValue          | `string` or `Array` | `AL`                                             |
| onValueChange          | `function`          | `()=>{`                                          |
| isMultiple             | `Boolean`           | `true`                                           |
| labelStyle             | `Object`            | `{backgroundColor: 'red', borderRadius: 0, ...}` |
| dropdownStyle          | `Object`            | `{backgroundColor: 'red', margin: 5, ...}`       |
| dropdownContainerStyle | `Object`            | `{backgroundColor: 'red', borderRadius: 0, ...}` |
| selectedItemStyle      | `Object`            | `{backgroundColor: 'red', color: 'yellow', ...}` |
| modalBackgroundStyle   | `Object`            | `{backgroundColor: 'blue', ...}`                 |
| modalOptionsContainer  | `Object`            | `{padding: 5}`                                   |

## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT
