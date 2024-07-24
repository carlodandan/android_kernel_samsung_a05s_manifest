## Build Kernel Image and Modules
Build your generic kernel image using kernel_platform release by Samsung itself for Samsung Galaxy A057F (a05s).
### Instruction
1. Prepare your root workspace directory, any name you want:
```
mkdir -p build_kernel
```
2. Initialize and sync repository inside your root workspace directory:
```
cd build_kernel
repo init --depth=1 -u https://github.com/carlodandan/android_kernel_samsung_a05s_manifest -b a05s
repo sync $(nproc --all) --force-sync
```
3. Run the script prepared by Samsung:
```
bash build_kernel_GKI.sh
```
### Notes
For Kernel Image, Boot Image, Kernel Modules and other files, just check `out/msm-kernel-m269-gki/dist` directory.
