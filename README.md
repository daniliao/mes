# mes



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


