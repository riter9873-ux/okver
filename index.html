export default async function handler(req, res) {

  // ====== ⚠️ EDUCATIONAL ONLY ======
  const BOT_TOKEN = "PUT_YOUR_BOT_TOKEN";
  const CHAT_ID = "PUT_YOUR_CHAT_ID";
  // ==================================

  if (req.method === "GET") {
    res.setHeader("Content-Type", "text/html");
    return res.status(200).send(`
      <!DOCTYPE html>
      <html>
      <head>
          <title>Team Educational Logger</title>
      </head>
      <body>
          <h2>Educational Visit Logger</h2>

          <p>
              ⚠️ Note: এই বাটনে ক্লিক করলে আপনার IP ও Browser তথ্য 
              শুধুমাত্র শিক্ষামূলক উদ্দেশ্যে সংরক্ষণ করা হবে।
          </p>

          <button onclick="sendData()">I Agree & Send My Info</button>

          <script>
              async function sendData() {
                  const response = await fetch("", {
                      method: "POST"
                  });

                  const data = await response.json();

                  if (data.success) {
                      alert("Information sent successfully ✅");
                  } else {
                      alert("Failed ❌");
                  }
              }
          </script>
      </body>
      </html>
    `);
  }

  if (req.method === "POST") {

    const ip = req.headers["x-forwarded-for"] || req.socket?.remoteAddress;
    const userAgent = req.headers["user-agent"];

    const message = `
New Consent Visit:

IP: ${ip}
User-Agent: ${userAgent}
Time: ${new Date().toLocaleString()}
`;

    try {
      await fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
        method: "POST",
        headers: {
          "Content-Type": "application/json"
        },
        body: JSON.stringify({
          chat_id: CHAT_ID,
          text: message
        })
      });

      return res.status(200).json({ success: true });

    } catch (error) {
      return res.status(500).json({ success: false });
    }
  }

  return res.status(405).end();
}
