# LibreTranslate

[Try it online!](https://libretranslate.com) | [API Docs](https://docs.libretranslate.com) | [Community Forum](https://community.libretranslate.com/) | [Bluesky](https://bsky.app/profile/libretranslate.com)

[![Python versions](https://img.shields.io/pypi/pyversions/libretranslate)](https://pypi.org/project/libretranslate) [![Run tests](https://github.com/LibreTranslate/LibreTranslate/workflows/Run%20tests/badge.svg)](https://github.com/LibreTranslate/LibreTranslate/actions?query=workflow%3A%22Run+tests%22) [![Build and Publish Docker Image](https://github.com/LibreTranslate/LibreTranslate/actions/workflows/publish-docker.yml/badge.svg)](https://github.com/LibreTranslate/LibreTranslate/actions/workflows/publish-docker.yml) [![Publish package](https://github.com/LibreTranslate/LibreTranslate/actions/workflows/publish-package.yml/badge.svg)](https://github.com/LibreTranslate/LibreTranslate/actions/workflows/publish-package.yml) [![Awesome Humane Tech](https://raw.githubusercontent.com/humanetech-community/awesome-humane-tech/main/humane-tech-badge.svg?sanitize=true)](https://codeberg.org/teaserbot-labs/delightful-humane-design)

Free and Open Source Machine Translation API, entirely self-hosted. Unlike other APIs, it doesn't rely on proprietary software such as Google or Azure to perform translations. Instead, its translation engine is powered by the open source [Argos Translate](https://github.com/argosopentech/argos-translate) library.

![Translation](https://github.com/user-attachments/assets/457696b5-dbff-40ab-a18e-7bfb152c5121)

## Getting Started

- [Quickstart](https://docs.libretranslate.com/)
- [Usage Instructions](https://docs.libretranslate.com/guides/api_usage/)
- [Community Resources](https://docs.libretranslate.com/community/resources/)

## Deploy on Railway

This repository includes a `Procfile` compatible with Railway:

```bash
web: libretranslate --host 0.0.0.0 --port $PORT --load-only en,fr,es --threads 2
```

Recommended Railway environment variables:

- `PORT` (provided by Railway automatically)
- `LT_UPDATE_MODELS=false`
- `LT_FORCE_UPDATE_MODELS=false`

Notes:

- First startup downloads translation models and can take several minutes.
- `--load-only en,fr,es` limits model downloads for faster deploys. Adjust as needed.
- Use a persistent volume if you want to keep downloaded models between restarts.

## Credits

This work is largely possible thanks to [Argos Translate](https://github.com/argosopentech/argos-translate), which powers the translation engine.

## License

[GNU Affero General Public License v3](https://www.gnu.org/licenses/agpl-3.0.en.html)

## Trademark

See [Trademark Guidelines](https://github.com/LibreTranslate/LibreTranslate/blob/main/TRADEMARK.md)
