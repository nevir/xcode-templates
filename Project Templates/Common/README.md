Common Templates
================

Style Macros
------------

    ___I#___  Indentation by # levels
    ___OB#___ Opening brace on a line that is indented by # levels
    ___CB#___ Closing brace on a line that is indented by # levels (else statements, etc)
    ___P___   variable pointer style when used in a variable definition
    ___VP___  variable pointer style `* `, ` *`, `*` when used in a method
    ___RS___  space between return type and start of method signature
    ___VS___  space between variable type and name in a method signature

### All Together Now

```
- (SomeThing___VP___)___RS___someMethod:(id)___VS___arg and:(Thing___VP___)___VS___anotherArg___OB0___
___I1___SomeThing___P___ foo = (SomeThing___VP___)anotherArg;

___I1___[self doSomeStuffWithFoo:foo];
___I1___return foo;
}
```


Anatomy of a Source File
------------------------

All source files are built via a relatively strict ordering of node definitions.

### Objective-C Header

* [`file.h:headerCommentsSlash:[Description]` or `file:headerCommentsHash:[Description]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Code%20Style.xctemplate/TemplateInfo.plist#L305)
* [`file.h:importFramework:[Framework]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L99)
* [`file.h:import:[Header]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L102)
* [`file.h:interface:definition:[Superclass & Protocols]` or `file.h:interface:ivars:definition:[Superclass & Protocols]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L132)
* [`file.h:interface:ivars:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L141)
* [`file.h:interface:properties:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L145)
* [`file.h:interface:methods:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L145)

### Objective-C Source

* [`file.h:headerCommentsSlash:[Description]` or `file:headerCommentsHash:[Description]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Code%20Style.xctemplate/TemplateInfo.plist#L305)
* [`file.h:importFramework:[Framework]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L99)
* [`file.h:import:[Header]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L102)
* [`file.m:private:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L150)
* [`file.m:implementation:synthesize:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L176)
* [`file.m:implementation:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L179)
* [`file.m:implementation:section:[Section Name]:[Definitions]`](https://github.com/nevir/xcode-templates/tree/xcode-4.5/Project%20Templates/Common/Objective-C%20Code%20Style.xctemplate/TemplateInfo.plist#L111)
