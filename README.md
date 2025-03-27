# nginx-kubernetes-practice

## Aufgabe: Deployment eines Nginx-Webservers mit Kubernetes Ziel:

## Erstelle einen Pod, ein Deployment mit mehreren Replikaten und einen Service für Nginx in Kubernetes.

## Definiere alle Ressourcen in einer YAML-Datei.

1. Ressourcen definieren
   Erstelle eine YAML-Datei, die folgende Ressourcen enthält:
   Einen Pod mit Nginx.
   Ein Deployment mit 3 Replikaten für Skalierbarkeit.
   Einen Service vom Typ NodePort, um die Anwendung erreichbar zu machen.

2. Ressourcen in Kubernetes ausrollen
   Wende die YAML-Datei auf das Kubernetes-Cluster an.
   Überprüfe, ob das Deployment, die Pods und der Service erfolgreich erstellt wurden.
   Greife über Minikube oder den NodePort auf die Nginx-Anwendung zu.

3. Deployment skalieren
   Erhöhe die Anzahl der Replikate des Deployments auf 5. Überprüfe, ob die neuen Pods gestartet wurden.

   ```sh
kubectl scale deployment nginx-deploy --replicas=5
kubectl get pods
```

5. Ressourcen bereinigen
   Lösche alle erstellten Ressourcen über die YAML-Datei, um das Cluster aufzuräumen.

## Clean Up

```sh
kubectl delete ingress --all
kubectl delete service --all
kubectl delete deployment --all
kubectl delete persistentvolumeclaim --all
```
