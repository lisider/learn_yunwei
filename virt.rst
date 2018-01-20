虚拟化
=======

平台虚拟化（Platform Virtualization），针对计算机和操作系统的虚拟化。
资源虚拟化（Resource Virtualization），针对特定的系统资源的虚拟化，比如内存、存储、网络资源等。
应用程序虚拟化（Application Virtualization），包括仿真、模拟、解释技术等。



平台虚拟化技术
----------------
     通过使用控制程序（Control Program，也被称为 Virtual Machine Monitor 或 Hypervisor），隐藏特定计算平台的实际物理特性，为用户提供抽象的、统一的、模拟的计算环境（称为虚拟机）。虚拟机中运行的操作系统被称为客户机操作系统（Guest OS），运行虚拟机监控器的操作系统被称为主机操作系统（Host OS），当然某些虚拟机监控器可以脱离操作系统直接运行在硬件之上（如 VMWARE 的 ESX 产品）。运行虚拟机的真实系统我们称之为主机系统。

     平台虚拟化技术的应用
          服务器虚拟化主要是用于整合服务器的，用于提高服务器的利用率，减小机房的资源开销，如电力、制冷、空间等，当然从管理维护角度和服务器的容灾角度也是有提升的

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

Xen

KVM

Kyper-V



常见的平台虚拟化技术概念的区别
------------------------------

qemu
VMware
Xen
KVM
Kyper-V
qemu-kvm
virsh
libvirt
libvirtd

`虚拟化技术漫谈`_
----

.. _`虚拟化技术漫谈`: https://www.ibm.com/developerworks/cn/linux/l-cn-vt/
