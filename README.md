# Project description

Development of a [vhost-user-vsock application](https://wiki.qemu.org/Google_Summer_of_Code_2021#vhost-user-vsock_application) in rust and its integration with kata containers. This work was done during Google Summer of Code 2021.

# Merged PRs/ Code contributions

- https://github.com/rust-vmm/vhost/pull/52
- https://github.com/rust-vmm/vhost/pull/54
  - Summary
    - The above two PRs add structures for inflight queues used for inflight IO tracking  
- https://github.com/torvalds/linux/commit/e3ea110d6e796146920e1be0108464ebcf283ef7
  - Summary
    - Fixes a bug in the virtio-vsock driver in the linux kernel that prevented a vsock driver from sending a VIRTIO_VSOCK_OP_CREDIT_REQUEST packet 

# Pending PRs

- https://github.com/rust-vmm/vhost-user-backend/pull/20
  - Summary
    - Implements the functionality to exchange inflight IO queue memory regions as file descriptors.
  - TODO
    - Incorporate feedback from reviewers and get it merged into main.
- https://github.com/rust-vmm/vhost-device/pull/7
  - Summary
    - This PR implements the vhost-user-vsock device used for communication between applications running in a guest in a VM and on a host, outside the VM.
  - TODO
    - Incorporate feedback from reviewers.
    - Improve throughput of the device.
    - Get it merged into main.

# TODO Components

- Integration of the vhost-user-vsock device into kata containers.
- Add more tests into the vhost-user-vsock device once the testing framework for queues is ready.
