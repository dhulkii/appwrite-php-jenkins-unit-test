using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>") // Your project ID
    .SetKey("<YOUR_API_KEY>"); // Your secret API key

Messaging messaging = new Messaging(client);

Message result = await messaging.CreateEmail(
    messageId: "<MESSAGE_ID>",
    subject: "<SUBJECT>",
    content: "<CONTENT>",
    topics: new List<string>(), // optional
    users: new List<string>(), // optional
    targets: new List<string>(), // optional
    cc: new List<string>(), // optional
    bcc: new List<string>(), // optional
    attachments: new List<string>(), // optional
    draft: false, // optional
    html: false, // optional
    scheduledAt: "" // optional
);