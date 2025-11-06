<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Open in Microsoft Edge</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; padding: 40px; }
    h1 { color: #0078D7; }
    button {
      background-color: #0078D7; color: white; border: none;
      padding: 15px 25px; font-size: 18px; border-radius: 5px;
      cursor: pointer;
    }
    button:hover { background-color: #005A9E; }
    p { margin-top: 20px; font-size: 16px; }
  </style>
</head>
<body>
  <h1>Redirecting...</h1>
  <p>If you are not redirected automatically, click below to open in Microsoft Edge:</p>
  <button onclick="openInEdge()">Open in Edge</button>

  <script>
    const sharepointURL = "[https://yourcompany.sharepoint.com/sites/yourpage](https://worksite.sharepoint.com/sites/VLS-Digitalization/SitePages/AI-@-VLS---Work-AI.-Think-AI.-Speak-AI.aspx)";
    const edgeDeepLink = "microsoft-edge:" + sharepointURL;

    // Detect if browser is Edge
    const userAgent = navigator.userAgent.toLowerCase();
    const isEdge = userAgent.includes("edg");

    if (isEdge) {
      window.location.href = sharepointURL;
    } else {
      // Try auto-open in Edge
      window.location.href = edgeDeepLink;
    }

    function openInEdge() {
      window.location.href = edgeDeepLink;
    }
  </script>
</body>
</html>
