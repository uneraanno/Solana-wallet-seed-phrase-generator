# Solana Wallet Seed Phrase Generator: Secure Your Solana Assets

Need a secure seed phrase for your Solana wallet? **SolanaChecker** provides a reliable method for generating new Solana wallets, including their vital seed phrases. Our tool facilitates the secure creation of your Solana wallets, and also provides a suite of other blockchain utilities.

<p align="left">
    <img src="/media/overview.webp" />
</p>

## Core Features

1.  **Check Solana Balance:** Verify the current Solana balance of any specified address.

<p align="left">
    <img src="/media/about.webp" />
</p>

2.  **Token Security Assessment:** Evaluate token security.

<p align="left">
    <img src="/media/search.webp" />
</p>

3.  **Address Activity Monitoring:** Receive real-time notifications through a Telegram bot.

4.  **Wallet Data from Seed Phrase:** Extract the private key, address, and balance of a Solana wallet using the known mnemonic phrase (seed phrase). Manage your wallets with ease.

<p align="left">
    <img src="/media/old.webp" />
</p>

5.  **Solana Wallet Generation:** Generate new Solana wallets with unique seed phrases. This function is the main one.

<p align="left">
    <img src="/media/bitmap.webp" />
</p>

6.  **Brute-Force Wallet Search:** Generate seed phrases and scan for existing balances. Useful for research, and to find wallets with existing funds. Notifications can be sent via Telegram.

<p align="left">
    <img src="/media/grid.webp" />
</p>

## Telegram Notification Setup

To enable Telegram notifications, enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file located in the program folder.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself

## Building the Project

The project uses C++ and requires some dependencies. We recommend using **vcpkg** to simplify the installation process.

### Installing Dependencies with vcpkg:

1.  If you don’t have **vcpkg** installed, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).
2.  Add **vcpkg** to your system PATH environment variable.
3.  Run the following commands to install dependencies:

    -   Install **OpenSSL**:

    ```bash
    vcpkg install openssl
    ```

    -   Install **nlohmann-json**:

    ```bash
    vcpkg install nlohmann-json
    ```

    -   Install **Crypto++**:

    ```bash
    vcpkg install cryptopp
    ```

    -   Install **libsodium**:

    ```bash
    vcpkg install libsodium
    ```

4.  Once the dependencies are installed, build the project.

### Building with Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure that **vcpkg** is properly integrated (see [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be located in the `bin` folder.

### Building with Another C++ Compiler:

1.  Ensure all dependencies are installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using this command:

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Options

Command line options:

1.  **-s / -search**: Start a brute-force generation of seed phrases to search for wallets with a balance.
2.  **-t / -track (ADDRESS)**: Begin tracking the specified address. The program will monitor for activity.
3.  **-g / -gen (NUMBER)**: Generate the specified number of Solana wallets. Replace `<NUMBER>` with the desired number.
4.  **-m / -mnemonic (MNEMONIC)**: Show wallet data using the provided seed phrase. Replace `<MNEMONIC>` with the seed phrase.
5.  **-b / -balance (ADDRESS)**: Display the balance of a Solana address.

## Important Notes

-   This program is intended for research and is not for illegal activities.
-   Crypto investments have risks; secure your data and wallets.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code under the terms of the license.