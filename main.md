# Notes Extension Language (NEL)

## Types
|Type|Example|
|-|-|
|Integer|`int`|
|String|`string`|
|Float|`float`|

---

Append [] to a `Type` to make it an Array.

---

## Program Stucture

```cs
-> ExtensionName {
    -> Greet("Hello.", new int[] { 20, 20 });

    void Greet(string message, int[] margins) {
        App.Print(message, margins);
    }
}
```