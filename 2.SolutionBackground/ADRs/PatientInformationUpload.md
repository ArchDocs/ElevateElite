# Status

Accepted

# Context

Holistic snapshot of patient health needs to be sent to MyMedicalData at anytime by the medical staff.

# Evaluation Criteria

- Security
- Ease of use
- Data consistency

# Options

## Option 1

Nursing station could include filtering and other capabilities embedded on the device. This would enable nurses to perform comprehensive analysis of the patients.

### Benefits

* Nurses could perform more.

### Drawbacks

* Nursing station would become more complex.
* Data upload to MyMedicalData might be inconsistent between nurses who send the data.

## Option 2

Nursing station could have a simple upload button that uploads the snapshot of patient consolidated vitals signs to MyMedicalData.

### Benefits

* Easy to use for nurses
* Upload of data would be consistent between nurses who send the data.

### Drawbacks

* If some filtering or input from the nurse would be required the nursing station would not support this functionality.

# Decision

We decided to go with Option 2.

# Implications

Simple to implement on the hardware side of the nursing station. Any updates to the snapshot can be done by updating the software of the nursing station.
