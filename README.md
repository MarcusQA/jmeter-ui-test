# Summary

This is a project to show a basic performance test which uses JMeter to test a UI application.

# Performance tests

To run the UI tests, use the JMeter UI. Alternatively, to execute the tests from the command line run the following from the JMeter `bin` folder:
```
jmeter -n -t <path\to\.jmx\file> -l <path\to\output\results\.jtl\file> -f -e -o <path\to\folder\to\output\report\files>

# Example
jmeter -n -t ..\..\workspace\jmeter-ui-test\jmeter_ui_test.jmx -l ..\..\test-results\test-results.jtl -f -e -o ..\..\test-results\report
```
