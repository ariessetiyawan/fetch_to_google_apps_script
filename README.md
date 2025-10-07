# fetch_to_google_apps_script
how to use fetch to request post/get in google apps scripts
var payload={
  "data":"test",
  "status:1
}
const data = new URLSearchParams(toFormData(payload));
 let response = await fetch(urlappMain,{
    method: "POST",
    body:data,
  })
  .then(r => r.json())
  .then(async(res) => {
    console.log(res)
    return res
  })
  .catch(error => {console.error('Error:', error)});

#how to post Image and data
var url='https://xxxx.com/dsfsdfs?id=xx&st=0
var base64=""//image base64
fetch(url, {
    method: "POST",
      maxBodyLength: Infinity,
      headers: {
        'Content-Type': 'text/plain'
      },
        body: base64,
      })
      .then(response => {
        var data=response.json()
        console.log('resp response',JSON.stringify(data))
        return data;
      })
      .then(data => {
        console.log('resp data',JSON.stringify(data))
        app.preloader.hide()
        if (data.success){
          console.log('resp data',JSON.stringify(data))
        }
      })
			.catch(error => {console.error('Error:', error)});
