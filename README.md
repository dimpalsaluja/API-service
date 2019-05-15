## Welcome to GNANI API Service

Use our Api to convert your Speech to Text

Here is a quick set-up guide to integrate Gnani speech API into your system.

Gnani speech Api supports multiple languages:
- Kannada
- Hindi
- Indian English
- Tamil
- Telugu
- Gujarathi

## Authentication 
To get access to our Api's visit [Link](https://gnani.ai) to register yourself.

## Prequisites for setting up the API
1. At the time of registration the token,accesskey would have been mailed to your registered email id without which you will not be authenticated to access our api's
2. API URL : [Link](https://gnani.ai)
3. Audio Format Supported - Wav
4. Audio Sampling Rate - 16000 or 8000
5. Channels - Mono
6. Encoding Format - PCM 16 bit

### Note
Language Codes are as follows :
<table>
<colgroup>
<col width="30%" />
<col width="70%" />
</colgroup>
<thead>
<tr class="header">
<th>Field</th>
<th>Description</th>
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
- In your client grpc code , you are required to pass headers along with the audio chunks. The headers must contain token,accesskey sent to your email id , the language that you want to use ,audioformat and encoding type as key value pairs. The format to be followed is below : 
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
<td markdown="span">pcm 16 bit</td>
</tr>
  * We will be supporting different audio properties soon.
  
## Sample Code
Here are the list of sample codes for Python and Nodejs.
- Python :[Link]

We will be adding other languages soon.

### Support or Contact

If you are having trouble please raise an issue or mail to us at email_id
