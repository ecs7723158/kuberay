# 🔬 Research & Engineering Notes: kuberay

- **Date**: 2026-09-14 21:12:09
- **Upstream Repository**: [ray-project/kuberay](https://github.com/ray-project/kuberay)
- **Stargazers**: ★ 2679
- **Summary**: A toolkit to run Ray applications on Kubernetes

---

## 📌 Architectural Breakdown
今天完整掃了 KubeRay 的 RayCluster controller 與 worker autoscaler 邏輯，發現它在 heterogeneous GPU 節點調度上的 lifecycle 處理做得很細膩。

## ⚙️ Engineering Evaluation
與 K8s Custom Metrics API 及 Prometheus adapter 的整合界面相當開放，能很好地監控 actor 狀態與 pending task 堆積情況。

## 🚀 Action Items & Next Steps
先 fork 過來測試與自訂 metrics exporter 的相容性，準備拉進本地端測試叢集驗證 auto-healing 機制。
