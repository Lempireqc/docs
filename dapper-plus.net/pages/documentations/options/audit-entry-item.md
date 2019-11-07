# AuditEntryItem

## Description

The `AuditEntryItem` is a property of the `AuditEntry` class.

It represent metadata about a specific column:
- ColumnName
- NewValue
- OldValue

```csharp
namespace Z.BulkOperations
{
    /// <summary>An audit entry item.</summary>
    public class AuditEntryItem
    {
        internal string _columnName;
        internal object _newValue;
        internal object _oldValue;

        /// <summary>Gets or sets the name of the column.</summary>
        /// <value>The name of the column.</value>
        public string ColumnName
        {
            get { return _columnName; }
            set { _columnName = value; }
        }

        /// <summary>Gets or sets the new value.</summary>
        /// <value>The new value.</value>
        public object NewValue
        {
            get { return _newValue; }
            set { _newValue = value; }
        }

        /// <summary>Gets or sets the old value.</summary>
        /// <value>The old value.</value>
        public object OldValue
        {
            get { return _oldValue; }
            set { _oldValue = value; }
        }
    }
}
```

> HINT: The `AuditEntryItem` is in Z.BulkOperations namespace since the library is used under the hood.

## Example

In this example,

A BulkMerge will be performed and the code will display all `AuditEntry` information and they corresponding `AuditEntryItem` informations:
- 1 rows has been inserted
- 2 rows has been updated

```csharp
// ...code...
```

Try it: [.NET Framework](https://dotnetfiddle.net/XB5npF) | [.NET Core](https://dotnetfiddle.net/y4w1ZG)