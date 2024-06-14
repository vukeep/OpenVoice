# Использование

## Оглавление

- [Быстрое использование](#quick-use): прямое использование OpenVoice без установки.
- [Linux Install](#linux-install): только для исследователей и разработчиков.
    - [V1](#openvoice-v1)
    - [V2](#openvoice-v2)
- [Установка на других платформах](#install-on-other-platforms): неофициальное руководство по установке, подготовленное сообществом.

## Быстрое использование


OpenVoice V2 может быть на **любом языке**. OpenVoice может клонировать голос в этом речевом аудио и использовать его для разговора на нескольких языках. Для быстрого использования мы рекомендуем вам попробовать уже развернутые сервисы:

- [British English](https://app.myshell.ai/widget/vYjqae)
- [American English](https://app.myshell.ai/widget/nEFFJf)
- [Indian English](https://app.myshell.ai/widget/V3iYze)
- [Australian English](https://app.myshell.ai/widget/fM7JVf)
- [Spanish](https://app.myshell.ai/widget/NNFFVz)
- [French](https://app.myshell.ai/widget/z2uyUz)
- [Chinese](https://app.myshell.ai/widget/fU7nUz)
- [Japanese](https://app.myshell.ai/widget/IfIB3u)
- [Korean](https://app.myshell.ai/widget/q6ZjIn)

## Минимальная демонстрация

Для пользователей, которые хотят быстро попробовать OpenVoice и не требуют высокого качества или стабильности, нажмите на любую из следующих ссылок:

<div align="center">
    <a href="https://app.myshell.ai/bot/z6Bvua/1702636181"><img src="../resources/myshell-hd.png" height="28"></a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://huggingface.co/spaces/myshell-ai/OpenVoice"><img src="../resources/huggingface.png" height="32"></a>
</div>

## Установка Linux

Этот раздел предназначен только для разработчиков и исследователей, знакомых с Linux, Python и PyTorch. Клонируйте это репо и запустите

```
conda create -n openvoice python=3.9
conda activate openvoice
git clone git@github.com:myshell-ai/OpenVoice.git
cd OpenVoice
pip install -e .
```

Независимо от того, используете ли вы V1 или V2, вышеописанная установка будет одинаковой.

### OpenVoice V1

Скачайте контрольную точку с [здесь](https://myshell-public-repo-hosting.s3.amazonaws.com/openvoice/checkpoints_1226.zip) и распакуйте ее в папку `checkpoints`.

**1. Гибкое управление стилями голоса.**.
Пожалуйста, посмотрите [`demo_part1.ipynb`](../demo_part1.ipynb) для примера использования того, как OpenVoice позволяет гибко управлять стилем клонированного голоса.

**2. Кросс-языковое клонирование голоса**.
Смотрите [`demo_part2.ipynb`](../demo_part2.ipynb) для примера использования языков, встречающихся и не встречающихся в обучающем наборе MSML.

**3. Демонстрация Gradio.**. Здесь мы предоставляем минималистичную локальную демонстрацию Gradio. Мы настоятельно рекомендуем пользователям изучить `demo_part1.ipynb`, `demo_part2.ipynb` и [QnA](QA.md), если у них возникнут проблемы с демонстрацией gradio. Запустите локальную демонстрацию gradio с помощью команды `python -m openvoice_app --share`.


### OpenVoice V2

Скачайте контрольную точку с [здесь](https://myshell-public-repo-hosting.s3.amazonaws.com/openvoice/checkpoints_v2_0417.zip) и распакуйте ее в папку `checkpoints_v2`.

Установите [MeloTTS](https://github.com/myshell-ai/MeloTTS):
```
pip install git+https://github.com/myshell-ai/MeloTTS.git
python -m unidic download
```
для быстрого выполнения с powershell, используем строку:
pip install git+https://github.com/myshell-ai/MeloTTS.git; if ($?) { python -m unidic download }
```

**Демонстрационное использование.** Пожалуйста, посмотрите [`demo_part3.ipynb`](../demo_part3.ipynb) для примера использования OpenVoice V2. Теперь он поддерживает английский, испанский, французский, китайский, японский и корейский языки.


## Установка на других платформах

В этом разделе представлены неофициальные руководства по установке, составленные участниками сообщества разработчиков открытого кода:

- Windows
  - [Guide](https://github.com/Alienpups/OpenVoice/blob/main/docs/USAGE_WINDOWS.md) by [@Alienpups](https://github.com/Alienpups)
  - Вы можете внести свой вклад, если у вас есть лучшее руководство по установке. Мы включим вас в список здесь.
- Docker
  - [Guide](https://github.com/StevenJSCF/OpenVoice/blob/update-docs/docs/DF_USAGE.md) by [@StevenJSCF](https://github.com/StevenJSCF)
  - Вы можете внести свой вклад, если у вас есть лучшее руководство по установке. Мы включим вас в список здесь.
