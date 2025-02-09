# Summary

This is a project to show a basic performance test which uses JMeter to test a UI application.

# Running the test

You can run the test via the JMeter UI or via the command line. And you can run the test using default performance-test parameters or override the default values. To run the tests with overriding values, use "Generate JMeter command with overriding parameters.xlsx".

To execute the tests from the command line run commands from the JMeter `bin` folder. View the report in the defined report folder by double-clicking `index.html`.

In the examples below:
- I'm assuming a parent JMeter folder containing subfolders named `apache-jmeter-5.6.3`, `test-results` and `workspace`.
- the report will be available at `test-results\report\index.html`

## Using default values
```
jmeter -n -t <path\to\.jmx\file> -l <path\to\output\results\.jtl\file> -f -e -o <path\to\folder\to\output\report\files>

# Example
jmeter -n -t ..\..\workspace\jmeter-ui-test\jmeter_ui_test.jmx -l ..\..\test-results\test-results.jtl -f -e -o ..\..\test-results\report
```

## Overriding default values
```
jmeter -n -t <path\to\.jmx\file> -Jthreads=<number of threads> -Jduration=<duration in seconds> -Jtarget_throughput=<throughput> -Jrandom_delay=<delay in ms> -l <path\to\output\results\.jtl\file> -f -e -o <path\to\folder\to\output\report\files>

# Example
jmeter -n -t ..\..\workspace\jmeter-ui-test\jmeter_ui_test.jmx -Jthreads=2 -Jduration=120 -Jtarget_throughput=72 -Jrandom_delay=1000 -l ..\..\test-results\test-results.jtl -f -e -o ..\..\test-results\report
```
