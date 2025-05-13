# Enabling RISC-V CI in Open-Source Projects: Challenges and Solutions

*Author:* Marek Pikuła (Samsung R&D Institute Poland)

> The adoption of RISC-V as a viable architecture for open-source software development is gaining traction. However, a major challenge remains: ensuring continuous integration (CI) support for RISC-V in upstream projects. At Samsung R&D Institute Poland, we addressed this issue by enabling RISC-V CI for several Freedesktop.org (FDO) projects, including Pixman and GStreamer Orc, and we are currently extending our work to the Opus codec. This work presents our approach to enabling RISC-V CI in FDO projects, addressing the challenges of testing architecture-specific optimizations without native hardware support. We detail our implementation of Docker-based GitLab runners with QEMU emulation, enabling automated multi-architecture testing while minimizing infrastructure overhead. Our work not only enhances software quality by enabling automated testing for RISC-V but also provides a framework for future contributions to seamlessly integrate RISC-V into open-source CI ecosystems.

## Resources

On this website you can find all resources for my poster submission for [*RISC-V Summit Europe 2025*](https://riscv-europe.org/summit/2025/):

- [GitHub repository with all resources][here]
- [Extended abstract][abstract] ([PDF version][abstract-pdf])
- [Poster (PDF)][poster-pdf]

You can read my RISC-V Summit Europe 2024 summary with some more information about this project on my [blog].

[here]: https://github.com/MarekPikula/RISC-V-Summit-Europe-2025
[abstract]: abstract/index.html
[abstract-pdf]: abstract/abstract.pdf
[poster-pdf]: poster/poster.pdf

## Repositories

The CI setup is realized on both on Freedesktop.org GitLab infrastructure, and
on the GitLab.com:

- [ci-multiplatform @ FDO][ci-fdo]
- [ci-multiplatform @ GitLab.com][ci-gitlab]

An example usage of the CI templates is shown in the Pixman fork:

- [pixman @ FDO][pixman-fdo]

[ci-fdo]: https://gitlab.freedesktop.org/MarekPikula/ci-multiplatform/
[ci-gitlab]: https://gitlab.com/MarekPikula/ci-multiplatform/
[pixman-fdo]: https://gitlab.freedesktop.org/MarekPikula/pixman/-/tree/ci-external

> [!NOTE]
> All repositories are available as submodules in the `code` directory.
