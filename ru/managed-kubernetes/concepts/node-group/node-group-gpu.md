# Группы узлов с GPU

Вы можете создавать группы узлов кластера {{ k8s }} с графическими ускорителями (GPU). Узел создается из образа виртуальной машины, совместимой с GPU, — на ней установлены драйверы NVIDIA и [библиотеки CUDA](https://developer.nvidia.com/gpu-accelerated-libraries) для GPU-ускорения.

## Требования {#requirements}

* Версия {{ k8s }} не ниже 1.16.

  Чтобы использовать GPU, версия {{ k8s }} на кластере и группе узлов должна быть 1.16 или выше.
* Ненулевая квота GPU.

  По умолчанию в облаке установлена нулевая квота на использование ВМ с GPU. Чтобы изменить [квоту]({{ link-console-quotas }}), обратитесь в [техническую поддержку]({{ link-console-support }}).
* Кластер в зонах `ru-central1-a` и `ru-central1-b`.

  ВМ с GPU доступны в этих [зонах](../../../overview/concepts/geo-scope.md). Запрашивая [квоту]({{ link-console-quotas }}) GPU, учитывайте, в каких зонах вы собираетесь запускать кластеры {{ k8s }}.

## Тарификация {#pricing}

Чтобы запустить группы узлов с GPU, необходимы кластер {{ k8s }}, ВМ с GPU и трафик. Поэтому тарификация состоит из следующих частей:
* Использование мастера {{ k8s }} оплачивается по [правилам {{ k8s }}](../../pricing.md).
* ВМ с GPU — по [правилам {{ compute-short-name }}](../../../compute/pricing.md#prices-instance-resources).
* Исходящий трафик — по [правилам {{ vpc-name }}](../../../vpc/pricing.md).