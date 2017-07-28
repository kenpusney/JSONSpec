# JSONSpec structure & syntax

## Basic structure

JSONSpec describes both the schema and the semantics of a data/service,
it requires as much as possible info to build a rich specification.

A valid JSONSpec have following sections:
  - **`JSONSpec` header**, contains the basic infomations of this JSONSpec document: the version of spec standard, 
  - **`type` section**, contains the type information of the data
  - **`constraint` optional section**, which provides more specific constaint for provided data field.
  - **`doc` optional section**, contains the documents to describe related dta field.
  - **`typedefs` optional section**, contains internal type definitions.

## Types

#### Standard types

see `doc/stlib.md`

#### Composite types

 - **Arrays**: `"[<type>]"`;
 - **Objects**: `{ "<keys>": "<typespec>" (, "<keys>": "<typespec>") + }`

## Selector syntax

  - **IdSelector**: just the key of the field
  - **OptionalSelector**: `<key>?`, means the key can be optional
  - **TypeSelector**: `[<type>]`the key must match specifid type (typically string, with some specific constraints)
  - **AnySelector**: *, match any key
