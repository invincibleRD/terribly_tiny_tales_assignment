# Terribly Tiny Tales Assignment

This repository contains the source code for the Terribly Tiny Tales assignment. The assignment involves generating a word frequency histogram based on a text fetched from a remote source. The histogram is displayed using a bar chart and can be exported as a CSV file.
## App Link: [https://terribly-tiny-tales-assignment-three.vercel.app/](https://terribly-tiny-tales-assignment-three.vercel.app/)

## Components

The project consists of the following main components:

### `pages/index.js`

This component is the main entry point of the application and is responsible for rendering the user interface. It utilizes Next.js's page-based routing system, which means that this component will be rendered when the user visits the home page of the application.

The `index.js` component performs the following tasks:

1. Fetching the text from a remote source: When the user clicks the "Submit" button, an HTTP request is made to retrieve the text data from the following URL: `https://www.terriblytinytales.com/test.txt`. The response is then processed to extract individual words.

2. Calculating word frequency: The extracted words are processed to calculate the frequency of each word using a JavaScript object. The `wordFrequency` object keeps track of the frequency of each word encountered in the text.

3. Generating the word frequency histogram: The top 20 most frequent words are selected from the `wordFrequency` object. For each selected word, an object is created with the `word` and its corresponding `frequency`. These objects are stored in the `histogramData` state variable, which is used to render the bar chart.

4. Displaying the histogram: The bar chart is rendered using the `react-chartjs-2` library, which wraps the functionality of the `Chart.js` library. The `histogramData` is used to generate the chart data, and the chart is displayed in the UI.

5. Exporting the histogram as a CSV file: When the user clicks the "Export" button, the `handleExport` function is triggered. This function converts the `histogramData` into CSV format and creates a download link for the user to export the data as a CSV file.

The component utilizes CSS modules for styling, with the styles defined in the `styles/Home.module.css` file.

Note: The logic and UI for rendering the chart and exporting the data are conditionally displayed based on the state variable `viewSubmit`. When `viewSubmit` is `true`, the "Submit" button is displayed, and when `viewSubmit` is `false`, the histogram and "Export" button are displayed.



- `styles/Home.module.css`: CSS module containing the styling for the components in the `pages/index.js` file.

- `next.config.js`: Next.js configuration file.

- `package.json`: Contains project metadata, dependencies, and scripts.

- `README.md`: This file, providing an overview of the project and its components.

## Libraries and Plugins Used

The project utilizes the following libraries and plugins:

- [Next.js](https://nextjs.org/): A React framework for building server-rendered applications.

- [React](https://reactjs.org/): A JavaScript library for building user interfaces.

- [react-chartjs-2](https://www.npmjs.com/package/react-chartjs-2): A wrapper for Chart.js to render charts in React applications.

- [Chart.js](https://www.chartjs.org/): A JavaScript library for creating responsive and customizable charts.

- [file-saver](https://www.npmjs.com/package/file-saver): A library for saving files on the client-side.

## Getting Started

To run the project locally, follow these steps:

1. Clone the repository:
`git clone https://github.com/your-username/terribly_tiny_tales_assignment.git`

2. Navigate to the project directory:

3. Install the dependencies:

4. Start the development server:

5. Open your web browser and visit `http://localhost:3000` to see the application.

## Available Scripts

In the project directory, you can run the following scripts:

- `npm run dev`: Starts the development server.

- `npm run build`: Builds the production-optimized version of the application.

- `npm start`: Starts the production server.

- `npm run lint`: Runs the ESLint linter to check for code quality and formatting issues.


## Deployment
The application is deployed using [Vercel](https://vercel.com).

You can access the deployed version at: [https://terribly-tiny-tales-assignment-three.vercel.app/](https://terribly-tiny-tales-assignment-three.vercel.app/)

## License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.




