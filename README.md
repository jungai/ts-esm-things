# Poc

typescript can't transpile native node esm without extension

## Solution

in typescript 4.6 has experimental support for ECMAScript modules in nodejs [read](https://www.typescriptlang.org/docs/handbook/esm-node.html)

```json
// tsconfig.json
"compilerOptions": {
    "moduleResolution": "nodenext"
  },
```

```typescript
import {} from "somefile.js";
```
