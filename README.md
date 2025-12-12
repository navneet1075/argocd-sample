# argocd-sample


# Add notifications to other apps
kubectl annotate application <app-name> -n argocd \
  notifications.argoproj.io/subscribe.on-sync-failed.slack=aicore-grafana-alerts

# Check notification logs if issues arise
kubectl logs -n argocd deployment/argocd-notifications-controller -f

# Test notifications manually
argocd app sync <app-name>


