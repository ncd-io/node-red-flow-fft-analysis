# node-red-flow-fft-analysis
 Analyze Time series data through FFT

## IMPORTANT: Additional steps are required outside of the import the flow itself
 You will need to install the fft-js library into your ~/.node-red directory and alter your ~/.node-red/settings.js file.

### fft-js
You can find the fft-js library at https://www.npmjs.com/package/fft-js

Commandline installation is required. You can use the following commands:
cd ~/.node-red
npm install fft-js


### settings.js File
You will need to edit your settings.js file generally located in ~/.node-red/settings.js

Replace this section:
functionGlobalContext: {
    // os:require('os'),
},
with this:
functionGlobalContext: {
    fft: require('fft-js').fft,
    fftUtil: require('fft-js').util
},

Save the file and restart node-red
