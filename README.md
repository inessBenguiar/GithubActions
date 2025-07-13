# ⚙️ GitHub Actions CI/CD Pipeline

This repository demonstrates a **CI/CD pipeline using GitHub Actions**, developed as part of the *Outils de Génie Logiciel (OGL)* module at the Higher National School of Computer Science (ESI Algiers).

The workflow automates testing, analysis, building, deployment, and notifications for a Java project using **Gradle**, **SonarCloud**, and **MyMavenRepo**.

---

## 🔁 Workflow Stages

| Stage               | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| 🧪 **Test**          | Executes unit tests and uploads JUnit + Cucumber results                    |
| 🔍 **Code Quality**  | Performs static analysis via **SonarCloud** and checks Quality Gate status |
| 🛠️ **Build**         | Builds the `.jar` artifact and generates **Javadoc**                       |
| 📤 **Deploy**        | Publishes the `.jar` to MyMavenRepo using Gradle                           |
| 📢 **Notify**        | Sends status notifications via **Slack** and **Email**                     |

---
Includes:

* Secure secrets via GitHub Actions (`secrets.*`)
* Gradle commands (`test`, `build`, `javadoc`, `publish`)
* `jq` for SonarCloud Quality Gate checks
* Conditional logic for notification on success/failure

## 📄 Workflow File

The main pipeline is defined in:  
```yaml
.github/workflows/main.yml


> 📂 You can find the Jenkins version of this pipeline here: [integration-continue](https://github.com/inessBenguiar/integration-continue)
