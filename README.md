# Quick-Material3-TimePicker-Dialog for Android
Quick creation of a TimePickerDialog not yet part of (material3:1.3.0-alpha02), similar to DatePickerDialog provided in Material3 Library

# No TimePickerDialog available in Material 3?
As of material3:1.3.0-alpha02 there is not TimePickerDialog similar to DatePickerDialog so we have to create our own for similar behavior to the date picker provided.

# Example Usage

```


var showTimePickerState by remember {
        mutableStateOf(false)
    }
if (showTimePickerState) {
                TimePickerDialog(
                    onCancel = { showTimePickerState = false },
                    onConfirm = {
                        //Your confirm behavior here
                        val newTime = LocalTime(timePickerState.hour, timePickerState.minute)
                        showTimePickerState = false
                    },
                ) {
                    TimePicker(state = timePickerState)
                }
            }
```

![image](https://github.com/spectechular/Quick-Material3-TimePicker-Dialog/assets/11188935/ba3dfd70-de6d-43b9-b816-135c2a2b2e6f)
