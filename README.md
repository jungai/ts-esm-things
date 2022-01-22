# Poc

typescript can't transpile native node esm without extension

## Solution

1. in typescript 4.6 has experimental support for ECMAScript modules in nodejs [read](https://www.typescriptlang.org/docs/handbook/esm-node.html)

```json
// tsconfig.json
"compilerOptions": {
    "moduleResolution": "nodenext"
  },
```

```typescript
import {} from "somefile.js";
```

2. use [tsc-esm-fix](https://github.com/antongolub/tsc-esm-fix) see [here](https://github.com/jungai/ts-esm-things/blob/main/ts/exp/package.json)

```bash
tsc-esm-fix --tsconfig ./tsconfig.json --ext='.js'
```
