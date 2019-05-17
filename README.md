## Welcome to GNANI Api Service

Use our Api to convert your Speech to Text

Here is a quick set-up guide to integrate Gnani speech Api into your system.

Gnani speech Api supports multiple languages:
- Kannada
- Hindi
- Indian English
- Tamil
- Telugu
- Gujarathi

## Authentication 
To get access to our Api's visit [gnani.ai](https://gnani.ai/ApiRequest) to register yourself.

## Prequisites for setting up the API
1. At the time of registration the token,accesskey would have been mailed to your registered email id without which you will not be authenticated to access our api's
2. API URL : [asr.gnani.ai]
3. Audio Format Supported - wav
4. Audio Sampling Rate - 16k Hz
5. Channels - mono
6. Encoding Format - pcm 16 

### Note
Language Codes are as follows :
<table>
<colgroup>
<col width="30%" />
<col width="70%" />
</colgroup>
<thead>
<tr class="header">
<th>Language</th>
<th>Code</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">Kannada</td>
<td markdown="span">kan_IN</td>
</tr>
<tr>
<td markdown="span">English</td>
<td markdown="span">eng_IN</td>
</tr>
 <tr>
<td markdown="span">Tamil</td>
<td markdown="span">tam_IN</td>
</tr>
<tr>
<td markdown="span">Hindi</td>
<td markdown="span">hin_IN</td>
</tr>
<tr>
<td markdown="span">Telugu</td>
<td markdown="span">tel_IN</td>
</tr>
  <tr>
<td markdown="span">Gujarathi</td>
<td markdown="span">guj_IN</td>
</tr>
</tbody>
</table>

## How to setup the API
- In your client grpc code , you are required to pass headers along with the audio chunks. The headers must contain token,accesskey sent to your email id , the language that you want to use , audioformat and encoding type as key value pairs. The format to be followed is below : 
<table>
<colgroup>
<col width="30%" />
<col width="70%" />
</colgroup>
<thead>
<tr class="header">
<th>Key</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">token</td>
<td markdown="span">eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ</td>
</tr>
<tr>
<td markdown="span">lang</td>
<td markdown="span">eng_IN</td>
</tr>
 <tr>
<td markdown="span">acesskey</td>
<td markdown="span">7f550a9f4c44173a37664d938f1355f0f92a47a7</td>
 </tr>
 <tr>
<td markdown="span">audioformat</td>
<td markdown="span">wav</td>
</tr>
  <tr>
<td markdown="span">encoding</td>
<td markdown="span">pcm 16</td>
 </tr>
</tbody>
</table>

### Note 
- Your request will not be authenticated if you fail to add any of these headers to your request.
- We currently support streaming through GRPC and audio with the following properties:
<table>
<colgroup>
<col width="30%" />
<col width="70%" />
</colgroup>
 <tbody>
<tr>
<td markdown="span">Audio Format</td>
<td markdown="span">wav</td>
</tr>
<tr>
<td markdown="span">Encoding Format</td>
<td markdown="span">pcm 16 </td>
</tr>
</tbody>
</table>
  * We will be supporting different audio properties soon.

## Grpc Error codes 
<table>
<tbody>
 </tbody>
</table>
<table>
<colgroup>
<col width="30%" />
<col width="20%" />
<col width="50%" />
</colgroup>
 <tbody>
 <thead>
<tr class="header">
<th>Code</th>
<th>Number</th>
<th>Description</th>
</tr>
</thead>
<tr>
<td markdown="span">OK</td>
<td markdown="span">0</td>
<td markdown="span">No error. Request is processed.</td>
</tr>
<tr>
<td markdown="span">CANCELLED</td>
<td markdown="span">1</td>
<td markdown="span">Operation was cancelled by the caller.</td>
</tr>
<tr>
<td markdown="span">PERMISSION_DENIED</td>
<td markdown="span">7</td>
<td markdown="span">The caller does not have permission to execute the specified operation. This occur if there is any issue in the header sent by the caller.</td>
</tr>
<tr>
<td markdown="span">INTERNAL</td>
<td markdown="span">13</td>
<td markdown="span">This means that some invariants expected by the underlying system have been broken. You can fnd the custom error details sent through grpc_message.
 Example : grpc_message":"Token is Invalid!</td>
</tr>
  <tr>
<td markdown="span">UNAVAILABLE</td>
<td markdown="span">14</td>
<td markdown="span">The server is currently unavailable.</td>
</tr>
</tbody>
</table>

## Sample Code
Here are the list of sample codes for Python.
- [Python](https://github.com/gnani-ai/API-service/tree/master/grpc-codes/Python3-Client)

We will be adding other languages soon.

### Support or Contact

If you are having trouble please raise an issue or mail to us at email_id
