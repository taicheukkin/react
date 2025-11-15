Based on the video transcript, here is a comprehensive summary of working with Function Components, Props, and Event Handling in React.

### Summary: Function Components, Props, and Event Handling

#### 1. What are Props?
- **Definition:** Props (properties) are a mechanism to pass data from a **parent component** to a **child component**.
- **Nature:** Props are **immutable** (read-only). A child component cannot change the props it receives.
- **Analogy:** Works like a function parameter or an object containing attributes.

#### 2. How to Use Props
**Parent Component (Sending Data):**
- Pass data by setting attributes on the child component tag.
- Can pass static values or dynamic variables using curly braces `{}`.

```jsx
// Parent Component (App)
function App() {
  const employeeID = 111;
  return (
    <EmployeeData 
      name="John" 
      employeeId={employeeID} 
      departmentId={567} 
    />
  );
}
```

**Child Component (Receiving Data):**
- Receive props as a function parameter (conventionally named `props`).
- Access values using the dot operator (`props.attributeName`).

```jsx
// Child Component (EmployeeData)
function EmployeeData(props) {
  return (
    <h1>Hello, {props.name}</h1>
    <p>ID: {props.employeeId}</p>
  );
}
```

#### 3. Default Props
- Provide fallback values when parent doesn't pass certain props.
- Ensures consistent rendering and prevents errors.

```jsx
EmployeeData.defaultProps = {
  dept_name: "HumanResources"
};
```

#### 4. Key Principles of Props
- **Reusability:** Same component can be reused with different props.
- **Unidirectional Data Flow:** Data flows only from parent to child, making applications easier to debug.
- **Customization:** Components can be customized through props without changing their internal code.
- **Composition:** Complex UIs can be built by combining simpler components that communicate via props.

#### 5. Event Handling with Props and State
**Example Scenario:** Conditionally displaying salary increase information.

**How it Works:**
1. **State Management:** Use `useState` hook to manage boolean state (`showIncrease`).
2. **Event Handling:** Button click triggers function that updates state.
3. **Conditional Rendering:** UI changes based on the state value.
4. **Props Integration:** The increase amount is passed via props and displayed when state is `true`.

```jsx
function SalaryComponent({ increase }) {
  const [showIncrease, setShowIncrease] = useState(false);
  
  const handleClick = () => {
    setShowIncrease(true);
  };
  
  return (
    <div>
      <button onClick={handleClick}>
        Display Annual Salary Increase
      </button>
      {showIncrease && (
        <div>Increase: {increase}</div>
      )}
    </div>
  );
}
```

### Key Takeaways
- **Props enable parent-child communication** in one direction only.
- **Props are immutable** - children cannot modify received props.
- **Default props provide safety nets** for missing data.
- **Events can trigger state changes** that control what renders based on props.
- **The combination of props, state, and events** creates dynamic, interactive components.

This pattern of passing data down via props and handling user interactions through events and state is fundamental to building React applications with function components.
