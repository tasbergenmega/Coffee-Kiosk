# Assignment 2 — Factory Method & Abstract Factory

**Theme:** Coffee Kiosk
**Author:** <Tasbergen Medeu>

## Run


## Part A — Factory Method
- Product: `Drink` (`prepare()`, `describe()`)
- ConcreteProducts: `Espresso`, `Latte`, `Cappuccino`
- Creator: `CoffeeMachine` (`createDrink()` + `serve()`)
- ConcreteCreators: `EspressoMachine`, `LatteMachine`, `CappuccinoMachine`
- Client: `factorymethod.Main` — never creates products directly

## Part B — Abstract Factory
- Products: `Cup`, `Lid`, `Receipt`
- AbstractFactory: `CoffeeSetFactory`
- ConcreteFactories: `ClassicSetFactory`, `EcoSetFactory`
- Client: `CoffeeKiosk` receives the factory via constructor (composition)
- Family is selected once in `abstractfactory.Main#pickBrand`

## FM vs AF
- Factory Method — inheritance, **one** product.
- Abstract Factory — composition, a **family** of 3 products.

## SOLID
- OCP: a new drink / brand does not change existing clients.
- SRP: products, factories and client each have one job.

## Weak spot of AF
Adding a new product kind (e.g. `Sleeve`) breaks every concrete factory.

## When over-engineering
If there is only one variant and no plan for more, plain `new` is enough.
