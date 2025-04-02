# CopilotEmbedCode
Contains the code necessary to embed a Copilot Chatbot into a custom website



<!--
Place this code snippet into the header or footer file (or master page) of the website.   This will ensure that the Copilot Agent (Chatbot) appears on each page, and maintains session across pages.
Al Smith - April 2025
-->

<!-- Floating Chat Button -->
<div id="chatButton" style="
position: fixed;
bottom: 20px;
right: 20px;
background-color: #0078D4;
color: white;
padding: 12px 20px;
border-radius: 50px;
cursor: pointer;
z-index: 1000;
box-shadow: 0 4px 6px rgba(0,0,0,0.1);
">
💬 Ask Chip!!!
</div>

<!-- Chatbot Popup Modal -->
<div id="chatModal" style="
display: none;
position: fixed;
bottom: 80px;
right: 20px;
width: 400px;
height: 600px;
z-index: 1001;
box-shadow: 0 4px 12px rgba(0,0,0,0.3);
border-radius: 12px;
overflow: hidden;
">
<!-- Close Button -->
<div style="
  position: absolute;
  top: 8px;
  right: 8px;
  z-index: 1002;
  background-color: white;
  border-radius: 50%;
  padding: 5px;
  cursor: pointer;
  font-weight: bold;
  color: #000;
" onclick="document.getElementById('chatModal').style.display='none'">✖</div>

<!-- Copilot Iframe -->
<iframe
  src="https://gcc.powerva.microsoft.us/environments/45d5a584-c2c4-eebc-8e8a-980ea2625111/bots/cre28_chip/webchat?__version__=2"
  width="100%"
  height="100%"
  frameborder="0"
  style="border: none;">
</iframe>
</div>

<!-- Script to toggle the chat -->
<script>
document.getElementById('chatButton').addEventListener('click', function () {
  var chat = document.getElementById('chatModal');
  chat.style.display = (chat.style.display === 'none' || chat.style.display === '') ? 'block' : 'none';
});
</script>

<!--
End of Copilot Agent (Chatbot) code snippet.
Al Smith - April 2025
-->
