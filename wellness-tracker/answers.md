# Week 7 - Quick-fire answers and reflection

## Part B

1. **Props vs state:** Props are Read-only data passed into a component from the outside (like arguments passed to a function). State is a private data created and managed inside a component that can change over time in response to user actions or network requests.
2. **useState(1):** It returns an array of two things: the current value (1) and a function to update it. We start at 1 because the form begins on Step 1.
3. **setCount(count + 1):** React only knows something changed, and re-renders, when we use the setter. Changing `count` directly would not update the screen.
4. **onClick:** It runs a function when the user clicks the element, e.g. a button.
5. **onChange:** It runs a function every time the input's value changes (each keystroke), so we can save the new value in state.
6. **event.target.value:** `event.target` is the input that fired the event, and `value` is the text currently inside it.
7. **Controlled input:** An input whose `value` comes from state and whose `onChange` updates that state, so React is the single source of truth.
8. **step === 2 && (...):** If step equals 2, React renders what is inside the brackets. If not, it renders nothing. It is conditional rendering.
9. **Back keeps name and age:** The values are stored in state in the parent `App` component, which stays mounted. Only the step changes, so the data is not lost.
10. **Tailwind:** It is a CSS framework of utility classes (like `p-4`, `bg-teal-600`) used to style the interface.It handles looks.

## Part C - Reflection

When the user types in an input, its `onChange` handler runs and uses `event.target.name` and `event.target.value` to update the `form` object in state. Each input's `value` is read back from that state, so the inputs are controlled. A separate `step` state decides which screen shows, using conditions like `step === 2 && (...)`. Next and Back just call `setStep` with a new number, and because `form` lives in `App`, the values stay saved when moving between steps. On the summary screen, the same `form` values are displayed inside a list with `{form.name}`, `{form.age}`, `{form.sleep}` and `{form.water}`.
