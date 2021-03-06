---
title: oVirt 4.3.7 Release Notes
category: documentation
toc: true
authors: sandrobonazzola
---

<style>
h1, h2, h3, h4, h5, h6, li, a, p {
    font-family: 'Open Sans', sans-serif !important;
}
</style>

# oVirt 4.3.7 Release Notes

The oVirt Project is pleased to announce the availability of the 4.3.7 Second Release Candidate as of October 31, 2019.

oVirt is a free open-source distributed virtualization solution,
designed to manage your entire enterprise infrastructure.
oVirt uses the trusted KVM hypervisor and is built upon several other community
projects, including libvirt, Gluster, PatternFly, and Ansible.

This release is available now for Red Hat Enterprise Linux 7.7 and
CentOS Linux 7.7 (or similar).


To find out how to interact with oVirt developers and users and ask questions,
visit our [community page]"(/community/).
All issues or bugs should be reported via
[Red Hat Bugzilla](https://bugzilla.redhat.com/enter_bug.cgi?classification=oVirt).
The oVirt Project makes no guarantees as to its suitability or usefulness.
This pre-release should not to be used in production, and it is not feature
complete.


If you'd like to try oVirt as quickly as possible, follow the instructions on
the [Download](/download/) page.

For complete installation, administration, and usage instructions, see
the [oVirt Documentation](/documentation/).

For a general overview of oVirt, read the [About oVirt](/community/about.html)
page.

To learn about features introduced before 4.3.7, see the
[release notes for previous versions](/documentation/#previous-release-notes).

## RELEASE CANDIDATE

In order to install this Release Candidate you will need to enable pre-release repository.

`# yum install `[`http://resources.ovirt.org/pub/yum-repo/ovirt-release43-pre.rpm`](http://resources.ovirt.org/pub/yum-repo/ovirt-release43-pre.rpm)



## What's New in 4.3.7?

### Bug Fixes

#### VDSM

 - [BZ 1758094](https://bugzilla.redhat.com/1758094) <b>[downstream clone - 4.3.7] [scale] VMs unresponsive due to delayed getVolumeSize</b><br>
 - [BZ 1757697](https://bugzilla.redhat.com/1757697) <b>[downstream clone - 4.3.7] Reporting incorrect high memory usage, preventing VMs from migrating, high slab dentry</b><br>

#### OTOPI

 - [BZ 1754515](https://bugzilla.redhat.com/1754515) <b>[downstream clone - 4.3.7] get_otopi_python always prefers Python3 even when site-packages are Python2 on RHEL 7.7</b><br>

#### oVirt Engine

 - [BZ 1766666](https://bugzilla.redhat.com/1766666) <b>[z-stream clone - 4.3.7] [REST] VM interface hot-unplug right after VM boot up fails over missing vnic alias name</b><br>
 - [BZ 1730538](https://bugzilla.redhat.com/1730538) <b>Engine compares incorrect versions when deciding to attach Tools ISO to Windows VMs</b><br>
 - [BZ 1759461](https://bugzilla.redhat.com/1759461) <b>[downstream clone - 4.3.7] [IPv6 Static] Engine should allow updating network's static ipv6gateway</b><br>

### Other

#### VDSM

 - [BZ 1752866](https://bugzilla.redhat.com/1752866) <b>Wrong payload path when migrating from a 4.4 host to a 4.3 host</b><br>

#### imgbased

 - [BZ 1747410](https://bugzilla.redhat.com/1747410) <b>imgbased upgrade fails: Exception! mount: special device /dev/rhvh_name/rhvh-4.3.5.3-0.20190805.0+1 does not exist</b><br>

#### oVirt Engine

 - [BZ 1763109](https://bugzilla.redhat.com/1763109) <b>[downstream clone - 4.3.7] Fix invalid host certificates by filling-in subject alternate name during host upgrade or certificate reenrollment</b><br>
 - [BZ 1765161](https://bugzilla.redhat.com/1765161) <b>[downstream clone - 4.3.7] upgrade of host fails on timeout after 30 minutes</b><br>Default maximum timeout for an ansible-playbook executed from engine has been raised from 30 to 120 minutes. This timeout is defined using configuration option ANSIBLE_PLAYBOOK_EXEC_DEFAULT_TIMEOUT within /usr/share/ovirt-engine/services/ovirt-engine/ovirt-engine.conf. If administrators need to change that timeout they can create /etc/ovirt-engine/engine.conf.d/99-ansible-timeout.conf file with below content:<br><br>  ANSIBLE_PLAYBOOK_EXEC_DEFAULT_TIMEOUT=NNN<br><br>where NNN is number of minutes the timeout should be.

#### oVirt Provider OVN

 - [BZ 1744235](https://bugzilla.redhat.com/1744235) <b>Security group rules for remote prefix/group do not enable traffic</b><br>
 - [BZ 1691933](https://bugzilla.redhat.com/1691933) <b>/etc/sudoers.d/50_vdsm_hook_ovirt_provider_ovn_hook is missing the commands of ovirt_provider_ovn_vhostuser_hook</b><br>
 - [BZ 1725013](https://bugzilla.redhat.com/1725013) <b>vdsm-tool fails deploying fedora 29 host from el7 engine</b><br>
 - [BZ 1723800](https://bugzilla.redhat.com/1723800) <b>[OVN] Updating a router's 'admin_state_up' returns OK but does not change the property</b><br>

#### oVirt Host Dependencies

 - [BZ 1759015](https://bugzilla.redhat.com/1759015) <b>[downstream clone - 4.3.7] Add clevis RPMs to RHV-H image / repo</b><br>

### No Doc Update

#### oVirt Host Deploy

 - [BZ 1761798](https://bugzilla.redhat.com/1761798) <b>[downstream clone - 4.3.7] Remove usage of rpmUtils.miscutils</b><br>

#### Contributors

23 people contributed to this release:

	Andrej Cernek
	Bell Levin
	Dafna Ron
	Dominik Holler
	Eitan Raviv
	Evgheni Dereveanchin
	Gal Zaidman
	Jeffrey Cutter
	Joey
	Liran Rotenberg
	Martin Nečas
	Martin Perina
	Miguel Duarte Barroso
	Milan Zamazal
	Nir Levy
	Nir Soffer
	Ondra Machacek
	Sandro Bonazzola
	Vojtech Juranek
	Yedidyah Bar David
	Yuval Turgeman
	imjoey
	mmirecki
