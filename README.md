### Animation

The **@keyframes** at-rule is used to define the flow of a CSS animation. Within the @keyframes rule, you can create selectors for specific points in the animation sequence, such as 0% or 25%, or use _from_ and _to_ to define the start and end of the sequence.

@keyframes rules require a name to be assigned to them, which you use in other rules to reference. For example, the `@keyframes wheel { }` rule would be named wheel.

To define how your animation should start, create a 0% rule within your @keyframes wheel rule. The properties you set in this nested selector will apply at the beginning of your animation.

As an example, this would be a 12% rule:

```
@keyframes wheel {
   0% {
     transform: rotate(0deg);
   }
    100% {
     transform: rotate(360deg);
   }
}
```

Give the @keyframes wheel rule a 100% selector. Within that, set the transform to rotate(360deg). By doing this, your animation will now complete a full rotation.

The **animation-name** property is used to link a @keyframes rule to a CSS selector. The value of this property should match the name of the @keyframes rule. Give your `.wheel` selector an animation-name property set to wheel.

The **animation-duration** property is used to set how long the animation should sequence to complete. The time should be specified in either seconds `(s)` or milliseconds `(ms)`.

The **animation-iteration-count** property sets how many times your animation should repeat. This can be set to a `number`, or to `infinite` to indefinitely repeat the animation.

The **animation-timing-function** property sets how the animation should progress over time. There are a few different values for this property: `linear`, `ease`, `ease-in`, `ease-in-out`, `cubic-bezier()`

The **animation** property will set the `animation-name`, `animation-duration`, `animation-timing-function`, and `animation-iteration-count` properties in that order.
