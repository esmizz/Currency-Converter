# Currency Converter

A modern, responsive currency converter built with React and Vite.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [API Integration](#api-integration)
- [Installation](#installation)
- [Usage](#usage)
- [Components](#components)
- [State Management](#state-management)
- [Styling](#styling)
- [License](#license)

## Features
- Convert between a wide range of currencies
- Real-time exchange rates
- Dark mode toggle
- Responsive design for mobile and desktop
- User-friendly interface

## Tech Stack
- React 
- Vite
- Tailwind CSS
- ESLint
- ExchangeRate-API

## Project Structure
```
currency-converter/
├── public/
│   └── Currency.svg
├── src/
│   ├── components/
│   │   ├── AmountInput.jsx
│   │   ├── ConversionResult.jsx
│   │   ├── CurrencySelector.jsx
│   │   └── DarkMode.jsx
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .eslintrc.cjs
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```
## API Integration

The Currency Converter integrates with the ExchangeRate API to fetch real-time currency exchange data. API calls are handled via Axios and centralized in the `src/services/api.js` file. The main API functions include:

- `getExchangeRate`: Fetch the latest exchange rate for a pair of currencies.
- `getConvertedAmount`: Convert a specific amount from one currency to another.
- `getSupportedCurrencies`: Retrieve a list of all supported currencies.

These functions allow the Currency Converter to perform all necessary operations, such as displaying current exchange rates, converting amounts between currencies, and providing users with a list of available currencies to choose from.

The API key is stored securely as an environment variable and is not exposed in the codebase.


A simple and efficient currency conversion application built with React and Vite.

## Installation

1. Clone the repository:

```bash
git clone <https://https://github.com/esmizz/Currency-Converter>
cd Currency-Converter
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the root directory and add your TMDb API key:

```bash
VITE_TMDB_API_KEY=your_api_key_here
```

4. Start the development server:

```bash
npm run dev
```

5. Open <http://localhost:5173/> to view the application.


## Usage

- `Currency Selection`:Use the dropdown menus labeled "From" and "To" to select the currencies you want to convert between.
- `Amount Input`:Enter the amount you want to convert in the input field labeled "Enter Amount...".
- `Conversion`:The conversion result is automatically displayed below the input fields. You can also click the "Get Exchange Rate" button to manually trigger a conversion.
- `Dark Mode`:Toggle the switch in the top-right corner to switch between light and dark modes for comfortable viewing in different lighting conditions.
- `Responsive Design`:The application is fully responsive and can be used on both desktop and mobile devices.
- `Real-time Updates`:Exchange rates are fetched in real-time when you change currencies or amounts, ensuring up-to-date conversion results.

## Components

- `App.jsx`:The main component that orchestrates the entire application, managing state and API calls.
- `CurrencySelector.jsx`:Dropdown component for selecting currencies. Displays flags and currency codes.
- `AmountInput.jsx`:Input field for entering the amount to be converted.
- `ConversionResult.jsx`:Displays the result of the currency conversion, including loading states.
- `DarkMode.jsx`:Toggle switch for enabling/disabling dark mode across the application.

Each component is designed to be reusable and manages its own local state where appropriate. They are composed in App.jsx to create the complete Currency Converter interface.

## State Management

State in the Currency Converter application is managed using React's useState and useEffect hooks within the App.jsx component. The main states include:

- `fromCurrency`: The currency to convert from
- `toCurrency`: The currency to convert to
- `amount`: The amount to be converted
- `convertedAmount`: The result of the conversion
- `isDarkMode`: The current theme (light/dark) preference
- `error`: Any error messages from API calls
- `isLoading`: Loading state during API calls

These states handle:

- Currency selection for both "from" and "to" currencies
- Input amount for conversion
- Conversion results display
- Dark mode preference
- Error handling and display
- Loading state during conversions

The `useEffect` hook is used to trigger the exchange rate fetch when relevant states (currencies or amount) change, ensuring real-time updates of the conversion result.

## Styling

The Currency Converter application uses Tailwind CSS for styling, providing a utility-first approach to design:

- Tailwind CSS classes are used extensively in the `className` props of components for styling.
- The application features a responsive design that adapts to different screen sizes.
- A dark mode is implemented using Tailwind's dark variant, allowing for easy theme switching.
- Custom styles for the toggle switch are defined in `src/index.css`.
- The main container uses a gradient background in light mode and a solid color in dark mode.
- Components like buttons, inputs, and result displays use consistent styling for a cohesive look.

Example of Tailwind usage:

```jsx
<div className={`bg-[#4EEFB2] dark:bg-gray-800 p-7 rounded-lg shadow-xl max-w-md w-full transition-all duration-300`}>
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.



