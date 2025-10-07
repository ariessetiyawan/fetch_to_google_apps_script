# fetch_to_google_apps_script
how to use fetch to request post/get in google apps scripts
>var payload={<br/>
	"data":"test",<br/>
  	"status:1<br/>
}<br/>
const data = new URLSearchParams(toFormData(payload));<br/>
let response = await fetch(urlappMain,{<br/>
	method: "POST",<br/>
    body:data,<br/>
})<br/>
.then(r => r.json())<br/>
.then(async(res) => {<br/>
	console.log(res)<br/>
    return res<br/>
})<br/>
.catch(error => {console.error('Error:', error)});<br/>

## how to post Image and data
>var url='https://xxxx.com/dsfsdfs?id=xx&st=0<br/>
var base64=""//image base64<br/>
fetch(url, {<br/>
    method: "POST",<br/>
      maxBodyLength: Infinity,<br/>
      headers: {<br/>
        'Content-Type': 'text/plain'<br/>
      },<br/>
        body: base64,<br/>
      })<br/>
      .then(response => {<br/>
        var data=response.json()<br/>
        console.log('resp response',JSON.stringify(data))<br/>
        return data;<br/>
      })<br/>
      .then(data => {<br/>
        console.log('resp data',JSON.stringify(data))<br/>
        if (data.success){<br/>
          console.log('resp data',JSON.stringify(data))<br/>
        }<br/>
      })<br/>
	.catch(error => {console.error('Error:', error)});<br/>
