# Welcome to your Expo app 👋

## Get started

1. Install Expo Go on your phone
2. Install dependencies

   ```bash
   npm install
   ```

3. Start the app

   ```bash
   npx expo start
   ```

## Interview tasks - Comprehension

1. Write the order in which the logs will be output.

```
console.log(1);

new Promise((resolve) => {
  resolve(console.log(5));
});

console.log(6);

new Promise((resolve) => {
  console.log(2);
});

setTimeout(() => {
  console.log(3);
});

console.log(4);
```

2. Write the result of this console log

```
var i = 10;

var array = [];

while (i--) {
  array.push(function () {
    return i + i;
  });
}

console.log([array[0](), array[1]()]);
```

3. How can we extend number to make this example work?

```
const number = 1;

console.log(number.plus(2)); /// 3
```

4. Write a curry function that will make this work

```
const join = (a, b, c) => {
   return `${a}_${b}_${c}`
}

const curriedJoin = curry(join)

curriedJoin(1, 2, 3) // '1_2_3'

curriedJoin(1)(2, 3) // '1_2_3'

curriedJoin(1, 2)(3) // '1_2_3'
```

5. Write the order of the console logs

```
const Parent = ({ children }) => {
  useEffect(() => {
    console.log("useEffect Parent");
  }, []);

  console.log("render Parent");

  return <View>{children}</View>;
};

const ChildrenOne = () => {
  useEffect(() => {
    console.log("useEffect ChildrenOne");
  }, []);

  console.log("render ChildrenOne");

  return (
    <View>
      <Text>Children One</Text>
    </View>
  );
};

const ChildrenTwo = () => {
  useEffect(() => {
    console.log("useEffect ChildrenTwo");
  }, []);

  console.log("render ChildrenTwo");

  return (
    <View>
      <Text>Children Two</Text>
    </View>
  );
};

const ChildrenThree = () => {
  useEffect(() => {
    console.log("useEffect ChildrenThree");
  }, []);

  console.log("render ChildrenThree");

  return (
    <View>
      <Text>Children Three</Text>
    </View>
  );
};

const ParentTwo = ({ children }) => {
  useEffect(() => {
    console.log("useEffect ParentTwo");
  }, []);

  console.log("render ParentTwo");
  return <View>{children}</View>;
};

const App = () => {
  useEffect(() => {
    console.log("useEffect app");
  });

  console.log("render app");

  return (
    <View>
      <Parent>
        <ChildrenOne />
        <ParentTwo>
          <ChildrenThree />
        </ParentTwo>
        <ChildrenTwo />
      </Parent>
    </View>
  );
};
```

## Interview tasks - Writing - React Native

1. Create a simple form with a text input and a submit button that displays the entered text below the form when submitted.

2. Implement a basic todo list where you can:

   - Add new todos
   - Mark todos as complete
   - Delete todos

3. Create a simple counter app with two buttons:

   - One to increment the count
   - One to decrement the count
   - Display the current count
   - Add a reset button to set the count back to 0

4. Build a simple list view that:

   - Displays a list of items with titles and descriptions
   - Allows tapping on an item to view its full details
   - Has a button to add new items to the list
   - Implements smooth scrolling and item animations

5. Create a basic weather app that:

   - Shows the current temperature
   - Displays weather conditions in text format
   - Has a refresh button to update the weather data
   - Uses a mock API response for the weather data
   - Shows a 5-day forecast with temperature ranges

6. Implement a simple navigation system with:

   - A home screen
   - A details screen
   - A back button to return to the home screen
   - Pass data between screens

7. Refactor the todo list app to use a custom hook that:

   - Encapsulates all todo-related state and logic
   - Provides methods for adding, completing, and deleting todos
   - Makes the todo list component cleaner and more maintainable

8. Refactor the counter app to use useReducer that:
   - Defines clear actions for increment, decrement, and reset
   - Implements a reducer function to handle state updates
   - Demonstrates understanding of reducer pattern and state management

These tasks are designed to test fundamental React Native concepts including:

- State management
- Component lifecycle
- User input handling
- Navigation
- API integration
- UI/UX implementation
- Custom hooks
- List rendering
- Form handling
