# 🏦 LoanFlow (https://github.com/rycherkray/LoanFlow)

**LoanFlow** is a minimalist, end‑to‑end **loan‑origination demo** that shows how I build
event‑driven, cloud‑native systems with .NET 8, Angular 17, and Azure.

<img src="docs/media/loanflow-arch.svg" alt="architecture diagram" width="640"/>

> 🧠 **Why this repo exists**  
> Hiring panels often ask, *“Can you show real code that proves you know micro‑services, async messaging, and clean architecture?”*  
> LoanFlow is the answer: clone → run → see a loan request travel UI → API → Service Bus → Function → Cosmos DB in under 60 seconds.

## ✨ Key Features
| Capability | Snapshot impact |
|------------|-----------------|
| **Angular portal** submits loan data and polls status. | Demonstrates RxJS, reactive forms, and API integration. |
| **ASP.NET Core API** isolates domain logic via MediatR. | Clean Architecture + async/await best practices. |
| **Azure Service Bus** decouples write & processing paths. | Resilient to spikes; retry & DLQ policies configured. |
| **Azure Function** processes queue events server‑lessly. | Scales to zero; logs to App Insights. |
| **Cosmos DB** stores loan docs in a partitioned container. | NoSQL modelling for high‑volume fintech workloads. |
| **CI/CD** YAML deploys API to Azure App Service with Key Vault secrets. | Proof of DevOps ownership. |

## 🔧 Full Tech Stack
| Layer | Tech |
|-------|------|
| Frontend | Angular 17, TypeScript, RxJS |
| Backend | ASP.NET Core 8, C#, MediatR |
| Messaging | Azure Service Bus (queue) |
| Processing | Azure Functions (.NET 8) |
| Storage | Azure Cosmos DB |
| Security | Azure Key Vault |
| DevOps | Azure DevOps Pipelines |
| Testing | xUnit, SpecFlow (soon) |

## 🚀 Quick Start (dev)
```bash
git clone https://github.com/rycherkray/LoanFlow.git
cd LoanFlow

# backend
dotnet run --project src/LoanFlow.Api

# frontend
cd loanflow-portal
npm install
npm start         # proxy → https://localhost:5001
