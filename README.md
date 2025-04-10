# 🚀 Welcome to My K3s + FluxCD Homelab – Where Magic (Mostly) Happens!  

Hey there, fellow tech wizard! 👋 You've stumbled upon my **homelab Kubernetes playground**, powered by the lightweight might of **K3s** and the GitOps sorcery of **FluxCD**.  

This is where I attempt to **automate all the things**, occasionally break stuff (then frantically fix it), and pretend I’m a cloud architect while my pets judge me from the couch. 🐕🐈  

---

## ⚡ What’s Cooking in This Lab?  

- **K3s**: Because full-fat Kubernetes is for people who enjoy waiting.  
- **FluxCD**: Because `git push` should magically deploy things (or at least try to).  
- **Helm Charts**: For when YAML isn’t complicated enough.  
- **Persistent Storage**: Because losing data is only funny once.  
- **Networking Shenanigans**: Where `kubectl get pods` sometimes returns `¯\_(ツ)_/¯`.  

---
## ☕ What's Brewing in This Digital Speakeasy?  

### 🔐 **WireGuard Wonders**  
- **VPN so fast** it makes my ISP suspicious  
- **Zero config management** (thanks Flux, I owe you a beer)  
- **Always up** (except when it's not - check `systemctl status`)  

### 💌 **XMPP Shenanigans**  
- **Prosody server** keeping my chats more retro than my vinyl collection  
- **Federation enabled** (but let's be real, who's actually federating with me?)  
- **OMEMO encryption** because I like my messages like my coffee - private  

---

## 🤔 Why Should You Care?  

- **Learn from my firewall mistakes** (there's a reason my `/var/log/` is 20GB)  
- **Copy my configs** (they mostly work... sometimes)  
- **Laugh at my XMPP client struggles** (why won't this @#$%ing file transfer work?!)  
- **Marvel at how often `systemctl restart` fixes things**  

---

## 🏕️ This is where I:  
🔒 **Pretend I'm a security expert** (until `journalctl` says otherwise)  
💬 **Run a chat server for my 3 active contacts** (hi Mom!)  
🤦 **Break things in production** (it's not production if it's in my basement, right?)  

---

## 🛠️ Quick Start (a.k.a. "Abandon Hope All Ye Who Enter Here")  

## Prerequisites

- A Kubernetes cluster (K3s recommended)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Flux CD](https://fluxcd.io/docs/installation/) for GitOps
- [SOPS](https://github.com/mozilla/sops) and [Age](https://github.com/FiloSottile/age) for secret management

## GitOps with Flux CD

If you're using Flux CD for GitOps:

1. Install Flux in your cluster:

```bash
flux bootstrap github \
  --owner=yourusername \
  --repository=homelab \
  --branch=main \
  --path=clusters/k3s
```

2. Flux will automatically apply your configurations based on the repository structure.
