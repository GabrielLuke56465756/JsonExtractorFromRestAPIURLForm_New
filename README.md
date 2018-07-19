# JsonExtractorFromRestAPIURLForm
Only "application/x-www-form-urlencoded" Request Payload is supported

#### Prerequisites
Install jdk/jre 8

#### Usage:
  1. Add required headers in header.properties
  2. Add url form parameters in urlformparameters.csv
     - Note: 
          - First row will be header i.e., all coloumns in first first row will be key in formurl
          - Multiple rows will iterated
  3. Add required endpoint details in endpoint.csv
     - Note: 
          - First row will be header ( will have URL and Method type Post/Put only supported )
          - Multiple rows will iterated along with url form parameters ( i.e., if you have 2 rows in urlformparameters.csv then each endpoint will iterated 2 times with different parameters )
  4. Set the correct Authentication token in authentication.properties
     - ( reach me out [email: gabriel.luke56465756@gmail.com] if default Authentication token is not working )
  5. Add the json path which you want to extract in jsonpath.properties
  6. Set number of simultaneous threads to executed in parallel.properties
  7. Run the run.bat/run.sh OR runParallel.bat/runParallel.sh file to start execution
  8. Output will stored in output.csv
     - CSV output will be like this
        - RequestNo,URL,Method,{headers},{formparams},Statuscode,{jsonpath}
