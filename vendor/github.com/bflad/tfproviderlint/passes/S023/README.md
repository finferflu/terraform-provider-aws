# S023

The S023 analyzer reports cases of schema including `Elem` that should
be removed with incompatible `Type`.

## Flagged Code

```go
&schema.Schema{
  Elem: &schema.Schema{},
  Type: TypeBool,
}

&schema.Schema{
  Elem: &schema.Schema{},
  Type: TypeFloat,
}

&schema.Schema{
  Elem: &schema.Schema{},
  Type: TypeInt,
}

&schema.Schema{
  Elem: &schema.Schema{},
  Type: TypeString,
}
```

## Passing Code

```go
&schema.Schema{
  Type: TypeBool,
}

&schema.Schema{
  Type: TypeFloat,
}

&schema.Schema{
  Type: TypeInt,
}

&schema.Schema{
  Type: TypeString,
}
```
