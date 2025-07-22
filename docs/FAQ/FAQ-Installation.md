---
{
  "title": "Installation FAQ",
  "description": "Frequently asked questions about how to properly install Wasabi Wallet. This is the Wasabi documentation, an archive of knowledge about the open-source, non-custodial and privacy-focused Bitcoin wallet for desktop."
}
---

# Installation of Wasabi

## Installing the Package

### Where can I download Wasabi?

You can find the recent version of the compiled packages for Linux, Windows and Mac available on the official [wasabiwallet.io](https://wasabiwallet.io).
It's always best to download software directly from the official source acknowledged by the developers.
In order to preserve your network level privacy from the very first step on, please consider visiting the Tor onion service [wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).
The old versions of the software can be found in the [releases](https://github.com/WalletWasabi/walletwasabi/releases) of the GitHub repository, [here](https://github.com/WalletWasabi/walletwasabi) you also find the libre & open source code for when you want to [build it yourself](/using-wasabi/BuildSource.md).
Please take special care to verify the PGP signatures of zkSNACKs' PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt) over the software packages and code commits.

### Why is it important to verify PGP signatures?

:::danger
**Don't trust ~ verify.**
:::
These are not just empty words.
Self sovereignty is at the core of Bitcoin in general, and Wasabi specifically.
You have powerful tools at your disposal, yet they only work when used as they are designed.
Wasabi is tailor made so that you do **not** have to trust anyone, but you have the power to verify everything.

With PGP signatures you can verify that the software package you download is actually the one published/signed by the developers.
Every release of Wasabi is signed by the [zkSNACKs](https://zksnacks.com/) key, the company originally behind Wasabi.
You can verify that the PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt) is actually the one of [zkSNACKs](https://pgp.mit.edu/pks/lookup?op=vindex&search=0x856348328949861E) by exploring the [web of trust](https://en.wikipedia.org/wiki/Web_of_trust).
When you have a software package that was signed by this PGP public key, then you can be sure that this is an official release approved by the zkSNACKs key.
This protects you against malicious man in the middle attacks where bad guys give you a fake version of Wasabi with malicious code.

[![Watch the video](/Logo_without_text_with_bg_dark_with_yt.png)](https://youtu.be/psl35MisYxo?list=PLPj3KCksGbSZkVpgAZjAFfFp4D0SHLnFw)

### How can I verify PGP signatures?

On the [WasabiWallet.io](https://wasabiwallet.io) website you can download the packages of the latest release.
To verify the signature you also need to download the separate signature `.asc` file.
In the terminal, change the directory to the one with the downloaded files, and verify the signature with `gpg --verify` + the corresponding signature file name, depending on which operating system you are.

Everything is valid if it returns `Good signature from zkSNACKs` and that it was signed with the `Primary key fingerprint: ${zksnacksPublicKeyFingerprint}`.

For an in-depth guide for [Debian and Ubuntu](/using-wasabi/InstallPackage.md#debian-and-ubuntu), [other Linux](/using-wasabi/InstallPackage.md#other-linux), [Windows](/using-wasabi/InstallPackage.md#windows), and [macOS](/using-wasabi/InstallPackage.md#macOS) see the main documentation.

[![Watch the video](/Logo_without_text_with_bg_dark_with_yt.png)](https://youtu.be/mTrClVA_o5A)

### How do I install Wasabi on Debian and Ubuntu?

[Download](/FAQ/FAQ-Installation.md#where-can-i-download-wasabi) the most recent `.deb` package and the `.deb.asc` signature file from the [wasabiwallet.io](https://wasabiwallet.io) or the [Tor onion service](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).

![Download Wasabi Wallet for Debian](/DownloadDeb.png "Download Wasabi Wallet for Debian")

Verify the signature of the package with `gpg --verify Wasabi-${currentVersion}.deb.asc Wasabi-${currentVersion}.deb` and ensure that the software was signed by zkSNACKs' PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt).

Now install Wasabi with `sudo apt install ./Wasabi-${currentVersion}.deb`, and run it with `wassabee`.
Check out the main documentation for a [step-by-step guide](/using-wasabi/InstallPackage.md#debian-and-ubuntu).

[![Watch the video](/Logo_without_text_with_bg_dark_with_yt.png)](https://youtu.be/mTrClVA_o5A?t=122)

### How do I install Wasabi on other Linux?

[Download](/FAQ/FAQ-Installation.md#where-can-i-download-wasabi) the most recent `.tar.gz` package and the `.tar.gz.asc` signature file from the [wasabiwallet.io](https://wasabiwallet.io) or the [Tor onion service](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).

![Download Wasabi Wallet for Linux](/DownloadTar.png "Download Wasabi Wallet for Linux")

Verify the signature of the package with `gpg --verify Wasabi-${currentVersion}-linux-x64.tar.gz.asc Wasabi-${currentVersion}-linux-x64.tar.gz` and ensure that the software was signed by zkSNACKs' PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt).
Now install Wasabi with `sudo tar -pxzf Wasabi-${currentVersion}-linux-x64.tar.gz`, and run it with `./wassabee`.
Check out the main documentation for a [step-by-step guide](/using-wasabi/InstallPackage.md#other-linux).

### How do I install Wasabi on Windows?

[Download](/FAQ/FAQ-Installation.md#where-can-i-download-wasabi) the most recent `.msi` package and the `.msi.asc` signature file from the [wasabiwallet.io](https://wasabiwallet.io) or the [Tor onion service](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).

![Download Wasabi Wallet for Windows](/DownloadWindows.png "Download Wasabi Wallet for Windows")

The Wasabi package is signed and automatically verified on Windows upon installation.

![Wasabi Wallet Windows signature verification](/InstallWindowsSignature.png "Wasabi Wallet Windows signature verification")

Optionally, you can still verify the PGP signature of the package by `right-clicking on the signature file > More GpgEX options > Verify` and ensure the software was signed by zkSNACKs' PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt).
Now install Wasabi by double-clicking the `.msi` file.
Check out the main documentation for a [step-by-step guide](/using-wasabi/InstallPackage.md#windows).

### How do I install Wasabi on macOS?

[Download](/FAQ-Installation.md#where-can-i-download-wasabi) the most recent `.dmg` package and the `.dmg.asc` signature file from the [wasabiwallet.io](https://wasabiwallet.io) or the [Tor onion service](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).

![Download Wasabi Wallet for macOS](/DownloadMac.png "Download Wasabi Wallet for macOS")

The Wasabi package is signed and automatically verified on macOS upon installation.

Optionally, you can still verify the PGP signature of the package with `sudo gpg2 --verify Wasabi-${currentVersion}.dmg.asc` and ensure that the software has been signed by zkSNACKs' PGP public key [${zksnacksPublicKeyFingerprint}](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt).
Now install Wasabi by double-clicking the `.dmg` file.
Check out the main documentation for a [step-by-step guide](/using-wasabi/InstallPackage.md#macos).

[![Watch the video](/Logo_without_text_with_bg_dark_with_yt.png)](https://youtu.be/_Zmc54XYzBA)

### Why are there two different packages for macOS (intel and Apple Silicon)?

Intel and Apple Silicon are two different processors types that Apple uses for their computers.
These processors work a bit differently from each other. 
With the architecture that Wasabi uses, these two different processors need their own specific code binary in order to make it work.

### What happens when I install the wrong package for macOS?

Wasabi will crash on startup or run significantly slower than it should.
This will not harm your computer.

### Do I need to install Tor separately?

No, because Wasabi has Tor built into the software.
All Wasabi network traffic goes via Tor by default - no need to set up Tor yourself.

You can turn off Tor in the Settings.
Be careful, as this will compromise your privacy.
When you coinjoin over clearnet, the coordinator would know the links between your inputs and outputs based on your IP address.
When you broadcast a transaction over clearnet, the connected full node will know the link between your transaction and your IP address.

### Can I use Wasabi on Tails?

Since Wasabi version [2.0.8](https://github.com/WalletWasabi/WalletWasabi/releases/tag/v2.0.8) it is possible to run Wasabi on Tails.
To make it work, Wasabi should be started with the `--UseTor=EnabledOnlyRunning` start up parameter or specify `"UseTor": "EnabledOnlyRunning"` in the config file.
So Wasabi uses the existing Tor process, instead of starting a new one.

### Can I use Wasabi on Whonix?

Since Wasabi version [2.0.8](https://github.com/WalletWasabi/WalletWasabi/releases/tag/v2.0.8) it is possible to run Wasabi on Whonix.
To make it work, Wasabi should be started with the `--UseTor=EnabledOnlyRunning` start up parameter or specify `"UseTor": "EnabledOnlyRunning"` in the config file.
So Wasabi uses the existing Tor process, instead of starting a new one.

### What are the differences between the Debian/Ubuntu version and the "Other Linux" version?

`Debian/Ubuntu` version contains `.deb` package.
`Other Linux` version contains `.tar.gz` package.

The advantages of the .deb format is solely packaging related.
It installs Wasabi in your computer, so you're able to access it from start menu, remove it through apt, and so on.

The "Other Linux" option is just a generic install method not targeted to Debian/Ubuntu specifically but that works on it anyway because it is still linux.

There's no difference in the code, the same binaries are being delivered in different formats.

## Update Wasabi

### Why should I update Wasabi?

Wasabi is cutting edge software and is being worked on by the developers on a daily basis.
Once in a while (+- every month) all the changes/improvements are being released in a new Wasabi version.
The changes can contain (critical) bug fixes, small improvements, new features etc.
It's always a good idea to run (one of) the latest Wasabi versions.

### How do I check the current version of Wasabi?

In the GUI, go to the SearchBar at the top of the screen and click on `About Wasabi`. 
Here the current version of your Wasabi is displayed.

You can also verify the version using the command line by executing `wassabeed --version`.

Wasabi is cutting edge software, so it is well-advised to stay up-to-date.

### How do I know about a new version of Wasabi?

When a new major version [v2.X.X] has been released, you'll see an orange update icon in the bottom right, upon hovering over it you can see `Version 2.X.X is now available`.

![Wasabi Update Available](/UpdateAvailable.png "Wasabi Update Available")

Clicking on `Update` uses the default browser to go to the website, where you can download this new version.
There are occasional silent releases like [v2.X.X.X] which fix small issues, and these are not announced in the GUI, so you will not see the orange update icon.
The [website](https://wasabiwallet.io) always contains the most recent version.
All releases (major and minor) are announced on the social media like [X](https://x.com/wasabiwallet) and [Reddit](https://reddit.com/r/WasabiWallet/).

### How do I securely upgrade Wasabi?

To upgrade Wasabi, you need to download the new version.
Downloading and installing the newer Wasabi package will overwrite the previous one, while preserving your files like your wallets etc.
So to upgrade Wasabi, simply download and install the new version like at first install.

You can download the software build for the different operating systems on the main [website](https://wasabiwallet.io) or better over [Tor](http://wasabiukrxmkdgve5kynjztuovbg43uxcbcxn6y2okcrsg7gb6jdmbad.onion).
For extra security, it is reccommended to also download the signatures of the build and verify them with [zkSNACKs' PGP public key](https://github.com/WalletWasabi/WalletWasabi/blob/master/PGP.txt).
For step-by-step instructions, follow [this guide](/using-wasabi/InstallPackage.md) or see this video: [![Watch the video](/Logo_without_text_with_bg_dark_with_yt.png)](https://youtu.be/DUc9A76rwX4)

### What does `Auto download new version` in the settings mean?

If enabled, the software will automatically download the new version's installer upon a new release.
If disabled, the software will only signal, but not automatically download, that there is a new version available.

:::tip Auto download new version is currently only available for Windows and macOS
For Linux, this setting does not work.
A new version will have to be installed manually.
:::

### How does the `Auto download new version` work?

The software will automatically download the new version's installer upon a new release.
After it is downloaded and the signature is verified, the user can press "Update on Close" to run the installer when closing Wasabi.
The installer is downloaded using the Nostr Update Manager.

### How does the Nostr update manager work?

Since Wasabi version [2.0.6](https://github.com/WalletWasabi/WalletWasabi/releases/tag/v2.6.0) the Wasabi client is notified of a new release using Nostr, instead of previously used GitHub.

The client fetches the latest Nostr event from the hardcoded [Wasabi Nostr pubkey](https://njump.me/npub129hpcwy3h7uhpzwzts6utkt2p5st7lf4qpzp3d2j0p6z56lvkpgspngzeq) and when the signaled version is higher than the client, the client gets a notification that a new release is available.
The Nostr event also contains the source of where to (auto) download the release from.
This is to be independent of GitHub for both the new release signaling and the downloading of a release, in case GitHub becomes unavailable.
The current downloading source still remains to be GitHub.

The Nostr Update Manager fetches Nostr events every 24 hours and on application launch.

> When `Auto download new version` is disabled, Nostr is only used for the signaling that a new version is available.

> Wasabi does not connect to Nostr when Tor is disabled.

## Advanced Installation

### How do I compile Wasabi from source?

If you cannot wait until the next release, and you want to experience the most cutting-edge version of Wasabi, then you can [build the source code](/using-wasabi/BuildSource.md).

The only two required tools are [Git](https://git-scm.com/downloads) and [.NET ${dotnetVersion} SDK](https://dotnet.microsoft.com/download) for "Build apps".
You can download every line of the Wasabi code by `git clone https://github.com/WalletWasabi/WalletWasabi.git`, this will create a new directory called `WalletWasabi`.
In order to build and run the Wallet software, change directory to `cd WalletWasabi/WalletWasabi.Fluent.Desktop`.
Wasabi is written in C# with the .NET framework, and it is very easy to run it.
Simply execute `dotnet run` from the `WalletWasabi.Fluent.Desktop` folder.
You can update the master branch with `git pull`.

### How can I verify the deterministic build?

The guide for the deterministic builds can be found in the [WalletWasabi repository](https://github.com/WalletWasabi/WalletWasabi/blob/master/WalletWasabi.Documentation/Guides/DeterministicBuildGuide.md).

### My antivirus marks Wasabi Wallet as a virus. Am I downloading the right software?

After you have downloaded Wasabi from the [official website](https://wasabiwallet.io) or from the [official GitHub repository](https://github.com/WalletWasabi/WalletWasabi/releases), make sure you have [verified the PGP signatures](/FAQ/FAQ-Installation.md#how-can-i-verify-pgp-signatures).

If you have downloaded and verified digital signatures and your antivirus continues to report Wasabi as positive, you don't have to worry about anything; it is a false positive.

If you are still not sure, before starting Wasabi, you can check that it is safe by uploading and scan it via [VirusTotal](https://www.virustotal.com/).

:::tip
Remember to report Wasabi as a safe software/false positive to your antivirus.
In doing so you will help users who use the same antivirus.
:::

### Why is the executable called wassabee?

The most obvious thing would be to call the executable `Wasabi Wallet.exe` on Windows and `Wasabi Wallet` on Linux and Mac.

However launching Wasabi Wallet from certain terminals/command lines is problematic, so we should remove the spacing: `WasabiWallet`, and the case sensitivity differences between the operating systems can also cause issues, so that must go too: `wasabiwallet`.

But it's too long, it needs a faster way to launch: `wasabi`.

However this is too generic, it'll certainly cause conflicts, we need to make it unique: `wassabee`.

Also, this sounds awesome and is a [fun inside joke](https://www.youtube.com/watch?v=dLzFKx6ONZQ).
