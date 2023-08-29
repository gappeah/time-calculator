I created a function called `add_time` which takes three parameters:

1. A starting time in the 12-hour clock format, with either "AM" or "PM" at the end.
2. A duration time specified in hours and minutes.
3. (Optional) A starting day of the week, not case-sensitive.

The function calculates the result by adding the duration time to the start time and returns the updated time. If the result is the next day, it appends "(next day)" to the time. If it's more than one day later, it adds "(n days later)" where "n" is the number of days.

If a starting day of the week is provided, the function also displays the resulting day of the week after the time and before the number of days later.

I successfully handled various cases, making sure the formatting is accurate. I paid close attention to proper spacing and punctuation.

Here are some examples:

- Calling `add_time("3:00 PM", "3:10")` returns "6:10 PM".
- Calling `add_time("11:30 AM", "2:32", "Monday")` returns "2:02 PM, Monday".
- Calling `add_time("11:43 AM", "00:20")` returns "12:03 PM".
- Calling `add_time("10:10 PM", "3:30")` returns "1:40 AM (next day)".
- Calling `add_time("11:43 PM", "24:20", "tueSday")` returns "12:03 AM, Thursday (2 days later)".
- Calling `add_time("6:30 PM", "205:12")` returns "7:42 AM (9 days later)".

I completed this project without importing any Python libraries. I assumed valid start times and handled duration times with minutes less than 60. The hour component of the duration can be any whole number.

For development and testing, I wrote the code in `time_calculator.py` and utilized `main.py` to execute the `time_calculator()` function by clicking the "run" button. I confirmed the functionality of my code by using the provided unit tests in `test_module.py`, which were imported into `main.py` for automated testing.
