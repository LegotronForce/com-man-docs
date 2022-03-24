# Log4Water:EXPANDED
`Log4Water:EXPANDED` is a logger system that has a few useful functions, and can save to a file.

* [Logger (base class)](#logger)
    * [Logger.log(text: string): void](#loggerlogtextstringvoid)
    * [Logger.warn(text: string): void](#loggerwarntextstringvoid)
    * [Logger.error(text: string): void](#loggererrortextstringvoid)
    * [Logger.debug(text: string): void](#loggerdebugtextstringvoid)
    * [Logger.clear(): void](#loggerclearvoid)

## Logger

### logger.log(text: string): void
This function logs text using the `log` prefix.
* `text` - The text to output

### logger.warn(text: string): void
This function sends a warning message in the text using the `warn` prefix.
* `text` - The text to output

### logger.error(text: string): void
This function sends an error message in the text using the `error` prefix.
* `text` - The text to output

### logger.debug(text: string): void
This function sends a debug message in the text using the `debug` prefix. Only sends if the `debug` argument is set in the constructor.
* `text` - The text to output

### logger.clear(): void
Clears the console and writes a message in the log stating it cleared the screen.
