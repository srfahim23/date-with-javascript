// Date with Javascript 
// const currentDate = newDate();
// console.log(currentDate)

// Basic Javascirpt 
// Date Formatting Methods 

/*
Javascript provides a few built-in methods to formate dates convenniently. Let's take a look at some of these a human-readable string format.
 */

// const date = new Date();
// console.log(date.toDateString());

// toSString(): This method convers a Date object into a string represtation following the ISO 8601 format. 

// examplate.jsx 
// const date = new Date();
// console.log(date.toISOString());

// 3...  toLocaleDateString(): This method returns string represating the date portiion of a Date bject uing the system's local conventions.

// const date = new Date();
// console.log(date.toLocaleDateString());

// Custom Date Formatting in JavaScriopt 

/*
While the baic formatting method can be useful in cerntain scenarions , you might often need more control over the date format.

1..... string Concatension: One Approaach is to manually concatenate the different components of a date using string manipulation.
 */

// const date = new Date();
// const formateDate  = `${date.getDate()}-${date.getMonth() + 1}-${date.getFullYear()}`;

// console.log(formateDate);

// 2... Intl.DateTimeFormat: Javascript's Int object offers powerful formatting cpabilities through the DateTimeFormat object. It provides localization support and various options to format dates and times.

// const date = new Date();
// const formatter = new Intl.DateTimeFormat('en-US', {
//     dateStyle: 'short' 
// });
// const formattedDate = formatter.format(date);
// console.log(formattedDate);

/*
Using Intl.DateTimeFormat, you can specify the desired locale and various optons to format dates sprecisely as needed.
 */


/*
How to Handle Time Zones 
when workikng with Dates 

When working with dates, it's essential to consider time 
zones, especially when dealing with global applications 
or time-sensitive information.

JavaScript provides methods to handle time zones effectively: 

1... Time Zone Offset: The getTimezoneOffset() method 
of the Date object returns the difference in minutes between the local time zone and UTC . You can use 
this offset to adjust dates for specific time zones.


2... Displaying Time Zones: To display the time zone 
information alongside the date, you can use the toLocaleString() method with the appropriate options.
 */

// const date = new Date();
// const formattedDate = date.toLocaleString('en-US', {
//     timeZoneName: 'short' 
// });
// console.log(formattedDate);


/**
 Common Date Formatting patterns 

 Centain date formatting patters are commonly used. 
 Here are a few examples:

 1... Specific Date Format: To display a date in a specific format, such as DD/MM/YYYY, you can 
 use Intl, DateTimeFomat with the appropriate options .
 */

//  const date = new Date();
//  const formatter = new Intl.DateTimeFormat('en-US', {
//     day: '2-digit', month: '2-digit', year: 'numeric'
//  });

//  const formattedDate = formatter.format(date);
//  console.log(formattedDate);

// 2... Time Format: To format the time portaon of a date, you can use the hour, minute, and second options.

// const date = new Date();
// const formatter = new Intl.DateTimeFormat('en-US', {
//     hour: '2-digit', minute: '2-digit', second: '2-digit'
// });
// const formattedDate = formatter.format(date);
// console.log(formattedDate);


/*
How to Handle Date Input 

A part from formatting dates for display, it's essential handle user intput dates effectly , Here are a few considerations: 

1... Paring User Input : Use the Date.parse() method or external libaries like Moment.js or Luxon to parese user-provided dates into valid Date objects.

2... Validating User Input : Implement validation machanism to ensure the user's input adheres to the expeteded date format. Regular expressions or external libraries can help with this.


 */