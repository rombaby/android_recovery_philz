philz-recovery中文源码

CM-11

本人开源个人Recovery项目，也希望各位用到我的代码的时候能提到我的名字，多谢

作者：changyuet

感谢xiaolu大大提供汉化字库支持，感谢CM团队

    git clone -b master https://github.com/changyuet/recovery-philz.git

Now build with RECOVERY_VARIANT flag set to philz:

    . build/envsetup.sh && lunch && mka -j3 recoveryimage RECOVERY_VARIANT=philz

or

    export RECOVERY_VARIANT=philz
    . build/envsetup.sh && lunch && mka -j3 recoveryimage

or

    add to device BoardConfig.mk:
        RECOVERY_VARIANT := philz
    and run:
        build/envsetup.sh && lunch && mka -j3 recoveryimage

