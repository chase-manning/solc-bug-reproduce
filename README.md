# Replicating SOLC bug

The below outlines how to replicate the solc issue here:

## Steps to replicate

1. Install node
2. Install dependencies: `yarn` (or can use `npm`)
3. Run `node index.js`

### What should happen

After the line `Script finished running` is logged, the script should end immediately.

### What happens

After the line `Script finished running` is logged, the script runs for an additional 5 seconds doing nothing.

### Debugging

To verify this issue, try to comment out the line `const solc = require("solc");` in the file `index.js`.  
Or instead, try to import any other package.  
The delay will not be there with either of the above.
