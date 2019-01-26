###### Nishant Arora

# VMware Notes

### Virtualization:

VMware’s roots surround virtualization: running largely unmodified operating systems in "software computers", "virtual machines," or VMs. 

A __Virtual Machine__ is a software container that can run its own operating system and execute applications
like a physical machine. 

Roughly 80 percent of x86 server workloads are now virtualized, and the average server runs 16 simultaneous VMs.

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
    * Unlike Bootcamp, it is not a dual boot setup so both OSs are run side by side. Slightly lesser performance but greater portability and ease of use.
    * Can still access data between Windows and Mac. Bootcamp needs setup to be able to read and write to NTFS.
    * Driver hardware for networking, audio, etc is virtualized natively with no extra setup.
* VMware ESXi
    * An enterprise software product that delivers greater performance than the freeware VMware Server due to lower system computational overhead. 
    * VMware ESXi is a "_bare-metal_" product that runs directly on the server hardware
    * Allows virtual servers to also use hardware more directly
* VMware Horizon Cloud
    * Enables the delivery of cloud-hosted or on-premises virtual desktops and apps to any device, anywhere, from a single cloud control plane.
    * Various deployment options:
        * Hosted infrastructure (from VMware)
        * Public cloud infrastructure  (Microsoft Azure)
        * On premises infrastructure
        * Combo of all 3
* vMotion
    * A technology that allows a running machine to move from one physical host to another without interruption of service.

### Virtual Desktop Infrastructure (VDI):

__VDI__ hosts a desktop operating system on a centralized server in a data center. VDI is a variation on the client-server computing model, sometimes referred to as server-based computing.

It is a desktop virtualization approach in which a desktop operating system, typically Microsoft Windows, runs and is managed in a data center. The desktop image is delivered over a network to an endpoint device, which allows the user to interact with the OS and its applications as if they were running locally. The endpoint may be a traditional PC, thin client or even a mobile device.

VDI can be Persistent or Non-Persistent

Persistent VDI:
* Provides each user with his or her own desktop image, which can be customized and saved for future use, much like a traditional physical desktop. 

Non-Persistent VDI:
* Provides a pool of uniform desktops that users can access when needed.
* Non-Persistent desktops revert to their original state each time the user logs out.

Benefits of VDI:
* Little actual computing takes place at the endpoint
    * IT departments may be able to extend the lifespan of otherwise obsolete PCs by repurposing them as VDI clients.
    * Organizations can buy cheaper, less powerful machines (thin-clients).
*  All data lives in the data center, not on the endpoint (security benefit)      
    * Ex. A thief who steals a laptop that uses VDI can't take any data off the machine, because there is no data on the machine. (hospitals, banks, govt, etc)

Drawbacks of VDI:
* Reliance on network connectivity 
    * Users can't access their virtual desktops without a network connection, and weak connectivity can hinder desktop performance
* Need to deal with software licensing and support
