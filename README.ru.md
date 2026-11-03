> English version: [README.md](README.md)

# LatteDrop

Личное macOS-приложение для real-time музыкальной визуализации в духе MilkDrop. Для себя, не публикуется: только macOS 26 и Apple Silicon, звук любого приложения через Core Audio Process Tap, рендер на Metal. Главный приоритет — точное попадание в бит, в том числе на AirPods.

Пока есть только техническое задание: [docs/SPEC.md](docs/SPEC.md) (v2.0 от 30 августа 2026). Порядок работ — этапы W0–W6 из раздела 10, первым идёт W0: Process Tap → RMS → цветной прямоугольник.
