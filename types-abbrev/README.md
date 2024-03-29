# Installation
> `npm install --save @types/abbrev`

# Summary
This package contains type definitions for abbrev (https://github.com/isaacs/abbrev-js#readme).

# Details
Files were exported from https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/abbrev.
## [index.d.ts](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/abbrev/index.d.ts)
````ts
// Type definitions for abbrev 1.1
// Project: https://github.com/isaacs/abbrev-js#readme
// Definitions by: BendingBender <https://github.com/BendingBender>
// Definitions: https://github.com/DefinitelyTyped/DefinitelyTyped

export = abbrev;

declare function abbrev(words: ReadonlyArray<abbrev.Abbreviable>): { [abbreviation: string]: string };
declare function abbrev(...words: ReadonlyArray<abbrev.Abbreviable>): { [abbreviation: string]: string };

declare namespace abbrev {
    function monkeyPatch(): void;

    type Abbreviable = string | { toString(): string };
}

declare global {
    interface Array<T> {
        abbrev(): { [abbreviation: string]: string };
    }

    interface ReadonlyArray<T> {
        abbrev(): { [abbreviation: string]: string };
    }

    interface Object {
        abbrev(): { [abbreviation: string]: string };
    }
}

````

### Additional Details
 * Last updated: Sun, 26 Sep 2021 14:31:24 GMT
 * Dependencies: none
 * Global values: none

# Credits
These definitions were written by [BendingBender](https://github.com/BendingBender).
