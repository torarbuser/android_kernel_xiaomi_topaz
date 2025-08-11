Branches:

    topaz-5.15.y-test-trash-2025-08-11
        - First attempt to merge topaz-t-oss into the fresh kernel
          The merge is done in a hasty manner; there may be serious bugs.
          It has not yet been tested on a phone, but it compiles successfully:
          using the command:
              cat ./build.config.gki.aarch64 > .config && \
              make ARCH=arm64 menuconfig && \
              make -j4 ARCH=arm64 CC="ccache aarch64-linux-gnu-gcc" \
                          CROSS_COMPILE="ccache aarch64-linux-gnu-"


Other branches:

    linux-5.15.y          - branch cloned from the kernel.org repo
    topaz-t-oss           - branch cloned from the GitHub MiCode repo
    android13-5.15-lts    - branch cloned from the android.googlesource.com repo
    android-msm-p11-5.15-tm-wear-kr3-dr-p11-qpr3-release
        - branch with the freshest Linux 5.15 source from Qualcomm repo
          (shares commit 0d019b5e4ac9 with topaz-t-oss)


Remotes:
android-googlesource https://android.googlesource.com/kernel/common.git
qcom                 https://android.googlesource.com/kernel/msm.git
linux-mainline       git://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git
xiaomi               https://github.com/MiCode/Xiaomi_Kernel_OpenSource.git
