## black_and_white rEFInd theme

[rEFInd](http://www.rodsbooks.com/refind/) is an easy to use boot manager for UEFI
based systems. This is a black_and_white theme for it.

![rEFInd black_and_white](https://github.com/yilmazdoga/rEFInd_black_and_white/blob/master/sample.png)

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed. `fdisk -l` and `mount` may help.

 2. Create a folder called `themes` inside it, if it doesn't already exist

 3. Clone this repository into the `themes` directory.

 4. To enable the theme add `include themes/rEFInd-black_and_white/theme.conf` at the end of
    `refind.conf`.

Here's an example menuentry configuration

```nginx

menuentry "Windows" {
	icon /EFI/refind/themes/rEFInd-black_and_white/icons/os_win.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/themes/rEFInd-black_and_white/icons/os_mac.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Entries that are autodetected should show the proper icons.
