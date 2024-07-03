# node-red-flow-fft-analysis
 Analyze Time series data through FFT

## IMPORTANT: Additional steps are required outside of the import the flow itself
 You will need to install the fft-js library into your ~/.node-red directory and alter your ~/.node-red/settings.js file.

### fft-js
You can find the fft-js library at https://www.npmjs.com/package/fft-js<br><br>

Commandline installation is required. You can use the following commands:<br>
```console
cd ~/.node-red
npm install fft-js
```


### settings.js File
You will need to edit your settings.js file generally located in ~/.node-red/settings.js<br><br>

Replace this section:<br>
functionGlobalContext: {<br>
    // os:require('os'),<br>
},<br>
with this:<br>
functionGlobalContext: {<br>
    fft: require('fft-js').fft,<br>
    fftUtil: require('fft-js').util<br>
},<br>
<br>
Save the file and restart node-red
