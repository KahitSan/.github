# Contributing to Kahitsan Solutions

Welcome! 🎉  
We’re excited that you want to contribute to our projects.  
This guide explains how we collaborate on frontend and backend projects in the organization.  

---

## 🛠 General Workflow

1. **Fork & branch**  
   - Always branch from `main` (or the default branch).  
   - Use feature branches: `feature/my-widget`, `fix/login-bug`.

2. **Commit style**  
   - Keep commits small and descriptive.  
   - Follow: `feat: add login widget`, `fix: incorrect token validation`.

3. **Pull Requests**  
   - Open a PR early (drafts are welcome).  
   - Provide context on what problem you’re solving.  
   - Expect code review before merge.

---

## 🎨 Frontend Guidelines

When creating a **new frontend application**:
- Use **Vite + SolidJS**.  
- Install and configure **TailwindCSS**.  
- Use our design system: [`kahitsan-ui`](https://github.com/KahitSan/kahitsan-ui).  

### Architecture (current vision)
- We’re moving towards a **modular micro frontend** architecture.  
- The goal: easily add new **widgets** (self-contained components with their own assets).  
- Each widget should be able to bring in its **CSS/assets** without breaking the rest of the app.  
- For now, follow the **standard SolidJS app structure** until the architecture matures.

---

## ⚙️ Backend Guidelines

- We follow a **modular architecture**:  
  - Harder to set up initially, but easier to maintain and remove modules later.  
  - Each service/module should be as independent as possible.  

### Communication Rules
- **Same machine** → prefer **Unix Domain Sockets (UDS)** or raw `net` sockets for fast IPC.  
- **Different machines** → use **HTTP(S)** with:  
  - **mTLS** (mutual TLS) for strong machine-to-machine authentication, or  
  - **JWT / API keys** if TLS termination happens at a gateway.  

---

## 🔮 Future Vision

- **Frontend:** Modular micro frontend with pluggable widgets.  
- **Backend:** Self-contained modules, communicating securely via IPC/HTTP.  
- Expect this document to evolve as we lock in final architectures.  

---

## ✅ How to Get Help

- Open an issue in the repo with `[Question]` in the title.  
- Ask in our internal chat (Slack/Discord/Teams/etc).  

Thanks for contributing 🚀
