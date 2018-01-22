虚拟化
=======

平台虚拟化（Platform Virtualization），针对计算机和操作系统的虚拟化。
资源虚拟化（Resource Virtualization），针对特定的系统资源的虚拟化，比如内存、存储、网络资源等。
应用程序虚拟化（Application Virtualization），包括仿真、模拟、解释技术等。



平台虚拟化技术
----------------
     通过使用控制程序（Control Program，也被称为 Virtual Machine Monitor 或 Hypervisor），
     隐藏特定计算平台的实际物理特性，为用户提供抽象的、统一的、模拟的计算环境（称为虚拟机）。
     虚拟机中运行的操作系统被称为客户机操作系统（Guest OS），
     运行虚拟机监控器的操作系统被称为主机操作系统（Host OS），
     当然某些虚拟机监控器可以脱离操作系统直接运行在硬件之上（如 VMWARE 的 ESX 产品）。
     运行虚拟机的真实系统我们称之为主机系统。

     平台虚拟化技术的应用
          服务器虚拟化主要是用于整合服务器的，用于提高服务器的利用率，
          减小机房的资源开销，如电力、制冷、空间等，
          当然从管理维护角度和服务器的容灾角度也是有提升的

虚拟化技术的分类
----------------

全虚拟化
超虚拟化
硬件辅助虚拟化
部分虚拟化
操作系统级虚拟化
半虚拟化




平台虚拟化技术的实现方案有几种
-------------------------

VMware
     在裸机上 和 在 系统上
     在系统上的虚拟化可以参考vmworkstation
     在裸机上的虚拟化可以参考 vm VSphere

Xen
     全虚拟化 和 半虚拟化

KVM
     用内核做虚拟机管理
     需要 Intel VT 或者 AMD-V 技术的支持
     egrep '(vmx|svm)' /proc/cpuinfo

Kyper-V



常见的平台虚拟化技术概念的区别
------------------------------

Xen
KVM
上面两种都是实现平台虚拟化的一种底层实现

qemu
这个也是一种 平台虚拟化的 实现, 这种实现 是 从底层到上层的,有底层 ,也有app

VMware
Kyper-V

qemu-kvm
这个是 kvm 上层的 app ,修改自qemu,可以控制 对平台的虚拟化

libvirt
这是是一个接口,位于 app 和 平台虚拟化的 底层实现 之间,可以 接口 Xen 和 KVM
Libvirt是管理虚拟机和其他虚拟化功能，比如存储管理，网络管理的软件集合。它包括一个API库，一个守护程序（libvirtd）和一个命令行工具（virsh）

virsh
这是利用libvirt api库 做的 一个 app
用来管理 Hypervisor 和 虚拟主机

virsh 命令，它是一个基于 libvirt 的命令套件，为创建和管理 libvirt 使用的所有对象—虚拟机（域）、存储卷、存储池、网络、网络接口、设备等提供了各个子命令。

virt-install
virt-install 命令，这是一个基于 libvirt api库  的命令，从名称可以看出，其设计宗旨是帮助从命令行创建虚拟机。


libvirtd
是libvirtd 的一部分

`虚拟化技术漫谈`_
----

`Linux 虚拟化技术`_
----------------------

.. _`Linux 虚拟化技术`: https://www.ibm.com/developerworks/cn/linux/theme/virtualization/

.. _`虚拟化技术漫谈`: https://www.ibm.com/developerworks/cn/linux/l-cn-vt/
