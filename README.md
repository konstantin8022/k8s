# k8s
pv

Применяем все вышеперечисленное в строго определенном порядке:

    SC
    PV
    PVC
    POD


# kubectl apply -f sc-local.yaml
# kubectl apply -f pv-local-node-1.yaml
# kubectl apply -f pvc-local.yaml
# kubectl apply -f pod-with-pvc-local.yaml

После этого посмотрите статус всех запущенных абстракций.

Проверим, что Local Persistent Volume правильно работает. Зайдем в под и создадим тестовый файл.

# kubectl exec -it pod-with-pvc-local sh
# echo "local srorage test" >> /mnt/local.txt

Теперь идем на сервер kub-node-1 и проверяем файл.
