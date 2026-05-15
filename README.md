# k8s-script

Repositori ini berisi manifest Kubernetes untuk menjalankan aplikasi Nginx sederhana di cluster Kubernetes.

## File Manifest

- **k8s-nginx-deployment.yaml**: Deployment untuk Nginx dengan 3 replicas, menggunakan image nginx:1.25.
- **k8s-Create-svc-clusterIP.yaml**: Service ClusterIP bernama "access" yang mengekspos port 8080 ke container port 80.
- **k8s-create-svc-nodePort.yaml**: Service NodePort bernama "access" yang mengekspos port 8080 ke container port 80.
- **k8s-nginx-ingress.yaml**: Ingress untuk mengakses aplikasi melalui host k8s.bagasproject.my.id pada path /.

## Cara Penggunaan

1. Pastikan Anda memiliki cluster Kubernetes yang berjalan.
2. Terapkan manifest deployment: `kubectl apply -f k8s-nginx-deployment.yaml`
3. Pilih salah satu service (ClusterIP atau NodePort): `kubectl apply -f k8s-Create-svc-clusterIP.yaml` atau `kubectl apply -f k8s-create-svc-nodePort.yaml`
4. Untuk akses eksternal via ingress, terapkan: `kubectl apply -f k8s-nginx-ingress.yaml` (pastikan ingress controller sudah terinstall)

## Modul Belajar
https://fopensource.univbanisaleh.my.id

## Referensi

Manifest dibuat oleh Bagas Maulana, referensi dari Aji Diyantoro YouTube.
