###### Nishant Arora

# VMware Notes

### Virtualization:

VMware’s roots surround virtualization: running largely unmodified operating systems in "software computers", "virtual machines," or VMs. 

A __Virtual Machine__ is a software container that can run its own operating system and execute applications
like a physical machine. 

VMs can do the following:
* Evaluate new apps and systems in a safe, partitioned environment
* Deploy and test your own software on multiple operating systems without needing multiple devices
* Set up and regulate encrypted corporate desktops for remote employees or employees using their own devices
* Run legacy programs that require an older OS on a machine with a newer OS
* Transfer virtual machines between devices and servers (vMotion)

Having a layer of software between the operating system and the physical hardware lets you tackle many ugly problems: 

* storage
* resource management
* fault isolation
* application management
 
None of these issues can be expected since they are not caused by a specific OS or application. VMware products such as vMotion can fix these issues on the fly.

### VMware Products:

* VMware Workstation
    * Allows users to run multiple instances of x86 or x86-64 compatible operating systems on a single physical personal computer. -- first product they released
    * Similar to Oracle's VirtualBox
* VMware Fusion
    * Virtualizes Windows operating systems and application programs so they can be used on Macintosh computers.
    * Unlike bootcamp, it is not a dual boot setup so both OSs are run side by side. Slightly lesser performance but greater portablilty and ease of use.
    * Can still access data between Windows and Mac. Bootcamp needs setup to be able to read and write to NTFS.
    * Driver hardware for networking, audio, etc is virualized natively with no extra setup.
* VMware ESXi
    * An enterprise software produc that delivers greater performance than the freeware VMware Server due to lower system computational overhead. 
    * VMware ESXi is a "_bare-metal_" product that runs directly on the server hardware
    * Allows virtual servers to also use hardware more or less directly
