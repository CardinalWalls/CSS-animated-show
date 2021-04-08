let html = document.querySelector("#html");
let style = document.querySelector("#style");

let content = `
#div1{
  width: 200px;
  height: 200px;

  border-radius: 30%;
  
  box-shadow: 0 0 3px rgba(0,0,0,0.5);
  /* border: none; */
  background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 50%, rgba(0,0,0,1) 50%, rgba(0,0,0,1) 100%);
  
}
#div1::before{
  width: 100px;
  height: 100px;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  background: #000;
  border-radius: 30%;
  background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 25%, rgba(0,0,0,1) 25%, rgba(0,0,0,1) 100%);
}
#div1::after{
  width: 100px;
  height: 100px;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  background: #fff;
  border-radius: 30%;
  background: radial-gradient(circle, rgba(0,0,0,1) 0%, rgba(0,0,0,1) 25%, rgba(255,255,255,1) 25%, rgba(255,255,255,1) 100%, rgba(0,0,0,1) 100%);
}
`;

let content_out = ''

function frame(n){
    setTimeout(
      ()=>{
        console.log(n)

        switch(content[n]){
          case "\n":
            content_out += '<br>';
            style.innerHTML = content.substring(0, n);
            html.scrollTo(0, 99999);
            break
          case ' ':
            content_out += '&nbsp'
            break
          default:
          content_out += content[n]
          html.innerHTML = content_out
        }

        if(n < content.length -1) frame(++n)
      }
      ,0)
}

frame(0)
