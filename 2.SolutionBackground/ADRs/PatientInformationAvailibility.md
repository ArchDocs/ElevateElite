# Status

Accepted

# Context

The system has a dependency to fetch the patient information, so that what ever the vital signs sents from the sensor devices can be mapped to the patient ID and other vital patient information to be displayed in Monitoring Dashboard, or to other views.

So it the patient information needs to be highly available. We assume we are getting the patient information from the SAAS cloud platform MyMedicalData.

But here we are trying to make it more highly available even though if MyMedicalData is unreachable(due to network error/App is down)

# Evaluation Criteria
- High Avaibility
- System shall work in any circumstances as the patient life is at risk, and no delay shall occur even if any component is down.

# Options

## Option 1

One solution is that there is an Patient onboarding App as part of MonitorMe solution, which can be used by Nurse to give the minimal information of the patient and the bed information. This way MonitorMe system can still function as normal. Whenever the MyMedicalData is reachable, we can sync up with MyMedicalData regarding the patient information.

### Benefits

* Highly available
* System works as long as MonitorMe functions

### Drawbacks

* More components in MonitorMe system
* Nurses might need to manually enter data and some data might be inconsistent
* Syncing the data between on-prem and cloud might be cumbersome and complicated.

## Option 2

One solution is to rely on MyMedicalData for all patient information. This solution has the drawback that if Internet connectivity is down patient information is not available and might cause issues with patient health monitoring.

### Benefits

* Easy to implement
* Low risk for data consistency issues

### Drawbacks

* If hospital doesn't have internet connectivity patient information might be outdated.

# Decision

We decided to go with Option 1.

# Implications

Additional component with UI interface and offline sync functionality need to be designed/implemented.
