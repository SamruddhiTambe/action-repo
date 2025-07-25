#  action-repo: GitHub Events Trigger Repository

- dummy-repo-for-webhook: GitHub activity repo to test webhook triggers.

- It serves as the **source of GitHub activity** (Push, Pull Request, and Merge events) which are captured via a webhook configured in the linked `webhook-repo`.

---

## 🔗 Connected To

This repository is connected to a Flask webhook server hosted in `webhook-repo`.

Webhook is configured under:

https://<your-ngrok-domain>.ngrok-free.app/webhook

---


---

## 🛠️ How It Works

- Any **Push**, **Pull Request**, or **Merge** action performed in this repo triggers a webhook to the Flask app.
- The webhook server then:
  - Captures event metadata
  - Stores the data in MongoDB
  - Displays it on a web UI

---

##  Events Triggered

| GitHub Action | Triggered | MongoDB Entry | UI Update |
|---------------|-----------|---------------|-----------|
| Push          |  Yes     |  Yes         |  Yes     |
| Pull Request  |  Yes     |  Yes         |  Yes     |
| Merge         |  Yes     |  Yes         |  Yes     |

---

##  Summary

- This repo is used only to generate GitHub activity.
- All actual webhook handling is implemented in the [webhook-repo](https://github.com/SamruddhiTambe/webhook-repo.git).
