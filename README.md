```
🏗️ Work in Progress...
```
This lesson will teach you:
- Running Jest unit tests
- Using unit tests to help debug code
- Writing Jest unit tests for existing code

The goal for this lesson is to learn a little about unit testing through the use of the [Jest Testing Framework](https://jestjs.io/).

In this case there are a few functions that are exported from the index.js file and have some tests written for them in the index.test.js file. 

For two of the functions the unit tests have already been written, but they are failing because of bugs in the code. In those cases you will be fixing the code to get the tests to pass.

For the third function the code is functional and you will be writing the body of the tests to test the functionality. An example of a test for that function already exists, as well as the names for the additional tests to write.

When you are done all of the tests, 8 in total, should be passing and you should have developed a basic feel for how to work with a testing framework like Jest to test code.

> While the code that is being tested does contain some simple math, none of the bugs are in the math itself.

> This project is using a different way to define modules from the ES6 `import` and `export` that you are familiar with already. This is just to keep the project as simple as possible and remove the need for a bundler like webpack. No changes should be needed in this area of the code.

# Instructions

## Fork the repository

The first step is to fork the source repository in GitHub and then clone your forked repository to your local development system. There are instructions for forking a repository in GitHub here: https://docs.github.com/en/get-started/quickstart/fork-a-repo


Once you have it cloned locally make sure that the application runs by running the following commands if you are using `yarn`:

> If you are using `npm` just replace `yarn` with `npm` and run the same commands.


```
yarn install
yarn test
```

## Familiarize yourself with the code

When you run the `yarn test` or `npm test` command it will use the Jest test runner to execute the tests in the index.test.js file. You should see 3 failing tests at this point (one is only passing by coincidence otherwise there would be 4). Take a few minutes to look over the output from the test runner because it is very useful in debugging why the tests are failing.

After each set of changes to the code you should run the test script again to see if the test results have changed.

Jest also support running in a `watch` mode that will watch the files under test for changes and rerun the tests when it detects the changes. To do this you can use the script target from the package.json file of `test:watch`. To run that script using yarn do `yarn test:watch`. To run that script with npm do `npm run test:watch`. Note the extra *run* text from the previous version for the npm command. If you use the watch script then you don't need to run `yarn test` at the end of each section because it will already be running.

If you want to attempt this on your own without a step by step walkthrough then leave the section below collapsed.

<details>
    <summary>Click the arrow to expand this section and see step by step instructions to fix the functions.</summary>

## Fixing the fahrenheitToCelsius function

- [ ] Open the `index.js` file and find the `fahrenheitToCelsius` function.
- [ ] There are two main bugs in this function. It is returning the wrong variable and it is not assigning the result of the computation to the new variable.
- [ ] Change the return value from `degreesFahrenheit` to `degreesCelsius`.
- [ ] Assign the result of the calculation to the `degreesCelsius` variable.
- [ ] Run `yarn test` to verify that the tests for this function are now passing.

## Fixing the celsiusToFahrenheit function

- [ ] Open the `index.js` file and find the `celsiusToFahrenheit` function.
- [ ] The bug in this function is subtle and could be easy to miss, but looking at the output from the test running should help point out what is wrong.
- [ ] The return value has a typo in the variable name. Change it to the correct variable name.
- [ ] Run `yarn test` to verify that the tests for this function are now passing.

## Writing tests for getFirstStringFromArray

There are 4 tests for this function. One of the tests has already been written to provide an example, but you will need to write the content for each of the 3 remaining tests.

- [ ] Using the `'Returns the first item if it is a string'` as an example write the test logic for the `'Returns null for an empty array'` test. You should pass in an empty array `[]` to the function for this test.
- [ ] Using the `'Returns the first item if it is a string'` as an example write the test logic for the `'Returns null if no strings are in the array'` test. Pass in an array containing only numbers for this test.
- [ ] Using the `'Returns the first item if it is a string'` as an example write the test logic for the `'Returns the second item if the first item is a number'` test. Pass in an array with a number followed by a string for this test.

</details>