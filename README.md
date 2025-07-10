# log4cxx.vcpkg

Este pacote NuGet fornece a biblioteca **log4cxx** versão **0.10.0**, compilada com o [vcpkg](https://github.com/microsoft/vcpkg) para **Windows x64** usando o **Microsoft Visual Studio 2022 (toolset v143)**.

## 📦 Conteúdo do pacote

- Arquivos de cabeçalho (`include/log4cxx/*.h`)
- Bibliotecas estáticas:
  - `log4cxx.lib`
  - `charset.lib`
  - `iconv.lib`
  - `lzma.lib`
  - `zlib.lib` (ou `zlibd.lib` no modo Debug)
- Bibliotecas dinâmicas (`.dll`) para Debug e Release
- Arquivo `.targets` que configura automaticamente:
  - Caminhos de include
  - Caminhos de biblioteca
  - Dependências
  - Cópia dos `.dll` para a pasta de saída (`$(OutDir)`)

## ⚙️ Como usar

1. Adicione o pacote ao seu projeto C++ via NuGet.
2. O Visual Studio aplicará automaticamente as configurações via o arquivo `.targets` incluído.
3. Certifique-se de que o projeto esteja em plataforma **x64**.

## 🔁 Configuração automática

- Em **Release**: links com `zlib.lib`
- Em **Debug**: links com `zlibd.lib`
- As DLLs são copiadas para `$(OutDir)` após o build

## 📝 Licença

- **log4cxx**: [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)
- Este pacote NuGet: [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)

## 🔗 Links úteis

- Site oficial: https://logging.apache.org/log4cxx/
- Fonte: https://github.com/apache/logging-log4cxx
- vcpkg: https://github.com/microsoft/vcpkg