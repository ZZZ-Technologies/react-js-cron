## ReactJS Cron

> A React cron editor with [antd](https://github.com/ant-design/ant-design) inspired by [jqCron](https://github.com/arnapou/jqcron)

[![npm package](https://img.shields.io/npm/v/react-js-cron/latest.svg)](https://www.npmjs.com/package/react-js-cron)

Live **demo** and **usage** at [https://xrutayisire.github.io/react-js-cron/](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--demo)

![react-js-cron example](https://raw.githubusercontent.com/xrutayisire/react-js-cron/master/react-js-cron-example.png)

## Features

- Zero dependencies except React and antd
- Supports all standard cron expressions
- Supports cron names for months and week days
- Supports cron shortcuts
- Supports "7" for Sunday
- Supports two-way sync binding with input
- Supports locale customization
- Supports multiple selection by double-clicking on an option
- And many more (disabled, read-only, 12-hour clock...)

## Installation

Be sure that you have these dependencies on your project:
* antd
* react
* react-dom

```bash
# Yarn
yarn add react-js-cron

# NPM
npm install --save react-js-cron
```

## Usage

Learn more with [dynamics settings](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--dynamic-settings).

- [Two-way sync binding with input](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--input)
- [Default value](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--default-value)
- [Default period](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--default-period)
- [Disabled mode](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--disabled)
- [Read-Only mode](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--read-only)
- [Humanized labels](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--humanize-labels)
- [Humanized value](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--humanize-value)
- [Leading zero for number](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--leading-zero)
- [Error management with text and style](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--track-error)
- ["Clear button" removal](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--no-clear-button)
- [Empty value management](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--empty-never-allowed)
- [Cron shortcuts](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--shortcuts)
- [12-hour clock](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--twelve-hour-clock)
- [24-hour clock](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--twenty-four-hour-clock)
- [Locale customization](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--french-locale)
- [Prefix and suffix removal](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--no-prefix-and-suffix)
- [Style customization](https://xrutayisire.github.io/react-js-cron/?path=/docs/reactjs-cron--custom-style)

## API

```
CronProps {
  value: string
  setValue: 
    | (value: string) => void
    | Dispatch<SetStateAction<string>> 
  className?: string
  humanizeLabels?: boolean // Default: true
  humanizeValue?: boolean // Default: false
  leadingZero?: boolean | ['month-days', 'hours', 'minutes'] // Default: false
  defaultPeriod?: 'year' | 'month' | 'week' | 'day' | 'hour' | 'minute' // Default: 'day'
  disabled?: boolean // Default: false
  readOnly?: boolean // Default: false
  allowEmpty?: 'always' | 'never' | 'for-default-value' // Default: 'for-default-value'
  shortcuts?: boolean // Default: true
  clockFormat?: '12-hour-clock' | '24-hour-clock'
  clearButton?: boolean // Default: true
  clearButtonProps?: ButtonProps // Extends antd button props without onClick
  displayError?: boolean // Default: true
  setError?: 
    | (error: {
      type: 'invalid_cron'
      description: string
    }) => void
    | Dispatch<SetStateAction<{
      type: 'invalid_cron'
      description: string
    }>>
    | undefined
  locale?: {
    everyText?: string
    emptyMonths?: string
    emptyMonthDays?: string
    emptyMonthDaysShort?: string
    emptyWeekDays?: string
    emptyWeekDaysShort?: string
    emptyHours?: string
    emptyMinutes?: string
    emptyMinutesForHourPeriod?: string
    yearOption?: string
    monthOption?: string
    weekOption?: string
    dayOption?: string
    hourOption?: string
    minuteOption?: string
    prefixPeriod?: string
    prefixMonths?: string
    prefixMonthDays?: string
    prefixWeekDays?: string
    prefixWeekDaysForMonthAndYearPeriod?: string
    prefixHours?: string
    prefixMinutes?: string
    prefixMinutesForHourPeriod?: string
    suffixMinutesForHourPeriod?: string
    errorInvalidCron?: string
    weekDays?: string[]
    months?: string[]
  }  // Default: See file 'src/locale.ts'
}
````

## License

MIT © [xrutayisire](https://github.com/xrutayisire)
  