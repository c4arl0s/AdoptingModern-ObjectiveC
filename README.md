# AdoptingModern-ObjectiveC

AdoptingModern-ObjectiveC

# instancetype

``` objective-c
@interface MyObject : NSObject
+ (instancetype)factoryMethodA;
+ (id)factoryMethodB;
@end
 
@implementation MyObject
+ (instancetype)factoryMethodA { return [[[self class] alloc] init]; }
+ (id)factoryMethodB { return [[[self class] alloc] init]; }
@end
 
void doSomething() {
    NSUInteger x, y;
 
    x = [[MyObject factoryMethodA] count]; // Return type of +factoryMethodA is taken to be "MyObject *"
    y = [[MyObject factoryMethodB] count]; // Return type of +factoryMethodB is "id"
}
```

For example:

``` objective-c
@interface MyObject
- (id)myFactoryMethod;
@end
```

should become:

``` objective-c
@interface MyObject
- (instancetype)myFactoryMethod;
@end
```




# Properties

# Enumeration Macros

# Object Initialization

# Automatic Reference Counting (ARC)

# Refactoring Your Code Using Xcode
