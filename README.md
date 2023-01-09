# Type Casting




**Type casting:**
```
class SuperClass { }
class SubClass1: SuperClass { }

class SubClass2: SuperClass {
    func nameMethod() {
        print("Ahmet")
    }
}


let objects = [SubClass1(), SubClass2(), SubClass1(), SubClass2()]

for object in objects {
    if let name = object as? SubClass2 {
        name.nameMethod()
    }
}
```

```
var stringProperty = "Alex"
if let property = stringProperty as? String {
    print("\(stringProperty)")
}
```

```
class SuperClass3 {
    var property = 3
}
class SubClass3: SuperClass3 { }
let subClassObject3 = SubClass3()
if let superObject3 = subClassObject3 as? SuperClass3 {
    print("\(superObject3.property)")
}


class SuperClass4 { }
class SubClass4: SuperClass4 {
    var property = 9
}
let superObject4 = SuperClass4()
if let superClassObject5 = superObject4 as? SubClass4 {
    print("The distance is \(superClassObject5.property).")
}
```
