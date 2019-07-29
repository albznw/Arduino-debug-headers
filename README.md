# Arduino debug headers

For easier Arduino debugging.

## How to install
Stand in your platformio project root and run the following commands.  
```sh
$ wget https://raw.githubusercontent.com/albzn540/Arduino-debug-headers/master/install.sh
```  
```sh
$ chmod +x install.sh
```  
```sh
$ ./install.sh
```

## How to use

``` cpp
// Initialize debugger
DebugInit(115200);

void testFunction() {
  Debugf("Debug message\n");
  // "Debug message"

  DebuFunc("Debug message\n");
  // "[testFunction()] Debug message"

  Err("Error message");
  // ERROR: Error message

  ErrFunc("Error message\n");
  // ERROR: [testFunction] Error message 
}
```