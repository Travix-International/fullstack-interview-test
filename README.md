**Travix - Problem to be solved**

You need to build a flight aggregator application. User input parameters: origin, destination, departure date, return date, number of passengers. It should search for flights with those parameters and show the list of flights to the user.

**Recommended duration of test:**

Allocate no more than 3 hours to complete this exercise. An incomplete solution is acceptable but documenting any remaining tasks and next steps is expected.

**FE Requirements:**

* React 16+
* Good state management
* Modular CSS
* Responsive design
* Linting
* Unit tests

It's possible to use a Create React App https://github.com/facebook/create-react-app 

**Backend:**

BusyFlights is a flight search solution that aggregates flight results initially from 2 different suppliers (CrazyAir and ToughJet). A future iteration (not part of the test) may add more suppliers.

**BE Requirements:**

Use this GitHub repository as a base to implement the Busy Flights service that should produce an aggregated result from both CrazyAir and ToughJet. It is fine to change any of the supplied application code. If you choose to do so, please add comments to indicate what has changed and why.
The result should be a JSON response which contains a list of flights ordered by fare.

The model attributes are the following:

**Busy Flights API**

**Request**

| Name | Description |
| ------ | ------ |
| origin | 3 letter IATA code(eg. LHR, AMS) |
| destination | 3 letter IATA code(eg. LHR, AMS) |
| departureDate | ISO_LOCAL_DATE format |
| returnDate | ISO_LOCAL_DATE format |
| numberOfPassengers | Maximum 4 passengers |

**Response**

| Name | Description |
| ------ | ------ |
| airline | Name of Airline |
| supplier | Eg: CrazyAir or ToughJet |
| fare | Total price rounded to 2 decimals |
| departureAirportCode | 3 letter IATA code(eg. LHR, AMS) |
| destinationAirportCode | 3 letter IATA code(eg. LHR, AMS) |
| departureDate | ISO_DATE_TIME format |
| arrivalDate | ISO_DATE_TIME format |

The service should connect to both the suppliers using HTTP.

**CrazyAir API**

**Request**

| Name | Description |
| ------ | ------ |
| origin | 3 letter IATA code(eg. LHR, AMS) |
| destination | 3 letter IATA code(eg. LHR, AMS) |
| departureDate | ISO_LOCAL_DATE format |
| returnDate | ISO_LOCAL_DATE format |
| passengerCount | Number of passengers |

**Response**


| Name | Description |
| ------ | ------ |
| airline | Name of the airline |
| price | Total price |
| cabinclass | E for Economy and B for Business |
| departureAirportCode | Eg: LHR |
| destinationAirportCode | Eg: LHR |
| departureDate | ISO_LOCAL_DATE_TIME format |
| arrivalDate | ISO_LOCAL_DATE_TIME format |

**ToughJet API**

**Request**

| Name | Description |
| ------ | ------ |
| from | 3 letter IATA code(eg. LHR, AMS) |
| to | 3 letter IATA code(eg. LHR, AMS) |
| outboundDate |ISO_LOCAL_DATE format |
| inboundDate | ISO_LOCAL_DATE format |
| numberOfAdults | Number of passengers |

**Response**

| Name | Description |
| ------ | ------ |
| carrier | Name of the Airline |
| basePrice | Price without tax(doesn't include discount) |
| tax | Tax which needs to be charged along with the price |
| discount | Discount which needs to be applied on the price(in percentage) |
| departureAirportName | 3 letter IATA code(eg. LHR, AMS) |
| arrivalAirportName | 3 letter IATA code(eg. LHR, AMS) |
| outboundDateTime | ISO_INSTANT format |
| inboundDateTime | ISO_INSTANT format |

**Note**

Please clone this project then create your own repository from it. Do not fork/branch this project when creating your solution as it will be visible to other applicants.
