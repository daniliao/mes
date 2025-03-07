# mes

You're encountering a permission issue because macOS restricts modifications to the system Ruby installation. Here are some solutions:

### **1. Use `sudo` (Not Recommended)**
You can install CocoaPods with admin privileges:
```sh
sudo gem install cocoapods
```
You'll be prompted for your password, but using `sudo` with system Ruby is not ideal.

### **2. Use a User-specific Gem Installation**
To avoid `sudo`, install gems in your home directory:
```sh
gem install --user-install cocoapods
```
Then add the following line to your shell configuration file (`~/.zshrc` or `~/.bashrc`):
```sh
export PATH="$HOME/.gem/ruby/2.6.0/bin:$PATH"
```
Restart your terminal or run:
```sh
source ~/.zshrc  # or source ~/.bashrc
```
Then retry:
```sh
cocoapods --version
```

### **3. Use a Ruby Version Manager (Recommended)**
macOS ships with an older system Ruby that is not ideal for development. A better solution is using `rbenv` or `RVM`:

#### **Using rbenv**
1. Install rbenv:
   ```sh
   brew install rbenv
   ```
2. Add it to your shell:
   ```sh
   echo 'eval "$(rbenv init -)"' >> ~/.zshrc
   source ~/.zshrc
   ```
3. Install a newer Ruby version:
   ```sh
   rbenv install 3.2.2
   rbenv global 3.2.2
   ```
4. Install CocoaPods:
   ```sh
   gem install cocoapods
   ```

Would you like help setting up `rbenv` or `RVM`?
