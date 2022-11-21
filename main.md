# Notes Extension Language (NEL)

## Types
|Type|Example|
|-|-|
|Integer|`int`|
|String|`string`|
|Float|`float`|
|Decimal|`decimal`|
|Structure|`struct`|

---

Append `[]` to a `Type` to make it an `Array`.

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

A NEL extension does not support classes or namespaces, and may be contained within a single file only.

## Reserved Keywords & Operators
`for`, `foreach`, `is`, `was`, `out`, `with`, `if`, `when`.

## Use of Events in an Extension
The following code will fire when the Printer has finished printing.

```cs
-> ExtensionName {
    -> NotifyUser when App.Printer.PrintingComplete;

    int[] printMargins: {
        20,
        20
    };

    -> App.Print("Text to print.", printMargins);

    void NotifyUser {
        out with "State: Printing complete.";
    }
}
```