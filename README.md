# IT313 Laboratory 4 - React Components & JSX in Action

## Student Roster Card Renderer
This laboratory demonstrates React Native functional components, JSX, props,
destructuring, conditional rendering, array mapping, and the key prop.

## Problem
The IT313 registrar provided a list of currently enrolled students. The goal
is to create an Expo React Native screen that displays each student using a
reusable StudentCard component.
Each card displays the student's name, course, units enrolled, and a Full Load
label when isFullLoad is true. The application also displays the total number
of enrolled students.

## Component Structure

### StudentCard
StudentCard is a reusable functional component. It receives name, course,
units, and isFullLoad as destructured props.

### StudentRoster
StudentRoster is the parent component. It contains the students array and
uses map() to render one StudentCard per student. Each card uses the student's
unique ID as its stable key.
The student count is computed from the array using roster.length.
## Key Experiment

The key was temporarily changed from key={student.id} to key={index}. The
Reverse Roster button was then used to reorder the students. In this simple
card, the visual result may still appear correct, but index keys are not
stable identities for dynamic lists. The key was then restored to
key={student.id}.

## How to Run
npm install
npx expo start
Then open the project with Expo Go.
## Technologies
- React Native
- Expo
- TypeScript
- JSX
- React Components