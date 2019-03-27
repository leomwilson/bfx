BFX files should compile to brainf\*\*\*. A Python implementation of this compiler will be included in this repository (github.com/leomwilson/bfx). This implementation will be the reference for these standards, and it will compile BFX programs exactly according to these standards. While other distributers may choose to further extend the functionality of BFX, these features will not have any official support.


To distinguish them from normal brainf\*\*\* programs, BFX files should use the extension .bfx


Lines that begin with `#` will not be added to the result, so they act like comments, even if they contain characters usually read by brainf\*\*\* (`+-<>[]`). This must be the first character of the line (it may not be preceeded by whitespace).


Lines using the extended functionality of BFX start with a `$` character. This must be the first character of the line (it may not be preceeded by whitespace). Lines not starting with `$` will be ignored by the BFX compiler, so they will be copied as-is to the result file. The syntax is as follows:
`$ <command> [options...]`


The following commands are supported, followed by their syntax:

`$ + <number>` OR `$ add <number>`

   Performs addition using the least number of characters possible.

   For example, `$ + 5` compiles to `+++++`

   For large additions, multiplication using loops will be used. The result depends on the current pointer, since pointer 0 is used for BFX array indexing.

`$ - <number>` OR `$ sub <number>`

   Similar to the above, but subtracts.
