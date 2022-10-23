<script src="numworks.js"></script>



<button id="connect">Connecter Numworks</button>
<div id="status"></div>
<div id="content">
            Please connect your Numworks.
 </div>
<!--add url input and associated validation button-->

 <!--add file input-->
<input type="file" id="file" name="file" accept=".py" /><br>
 <!-- add a multiline textbox -->
<textarea id="code" rows="10" cols="50"></textarea>
<br><button id="send">Envoyer</button>


<script>
var calculator = new Numworks();

var script = document.getElementById("code");

var status = document.getElementById("status");
var connect = document.getElementById("connect");
var content = document.getElementById("content");
var send = document.getElementById("send");
var file = document.getElementById("file");

navigator.usb.addEventListener("disconnect", function(e) {
  calculator.onUnexpectedDisconnect(e, function() {
    status.innerHTML = "Disconnected.";
    content.innerHTML = "Please connect your Numworks.";
    calculator.autoConnect(autoConnectHandler);
  });
});

//on file change, get text content and put it in the textarea
file.addEventListener("change", function(e) {
  var file = e.target.files[0];
  var reader = new FileReader();
  reader.onload = function(e) {
	script.value = e.target.result;
  };
  reader.readAsText(file);
});
//on send click, trigger handleScriptSend
send.addEventListener("click", handleScriptSend);

function handleScriptSend() {
    var code = script.value;
    connected(code, "mkdocs", 1);
}

calculator.autoConnect(autoConnectHandler);

function autoConnectHandler(e) {
  calculator.stopAutoConnect();
  connected("", "", 0);      
}

connect.onclick = function(e) {
  calculator.detect(function() {
    calculator.stopAutoConnect();
    connected("","",0);
  }, function(error) {
    status.innerHTML = "Error: " + error;
  });
};

async function connected(script, name, send) {
  connect.disabled = true;
  status.innerHTML = "Connected.";

  var model = calculator.getModel(false);

  var html_content = "Model: " + calculator.getModel(false) + "<br/>";

  // Get the platform information
  var platformInfo = await calculator.getPlatformInfo();
  console.log(platformInfo);
  if(send) {
  var storage = await calculator.backupStorage();
	storage.records.push({"name": name, "type": "py", "autoImport": true, position: 0, "code": script});
	await calculator.installStorage(storage, function() {
    console.log("don")
	});
  }
  content.innerHTML = html_content;
}
</script>