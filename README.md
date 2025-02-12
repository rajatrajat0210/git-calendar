# 🎨 Gitfiti: Custom GitHub Contribution Graph Art

Gitfiti lets you create custom artwork on your GitHub contributions graph by generating fake commits. Follow this guide to set it up on your own GitHub profile!

---

## 🚀 **Getting Started**

### **1. Install Python**
Make sure Python is installed by running:

```sh
python --version
```
If it's not installed, download it from [python.org](https://www.python.org/downloads/).

---

### **2. Clone the Gitfiti Repository**
Download Gitfiti by running:

```sh
git clone https://github.com/gelstudios/gitfiti.git
cd gitfiti
```

---

### **3. Create a New GitHub Repository**
1. Go to [GitHub](https://github.com/new).
2. Create a new repository (leave it empty, no README, .gitignore, or license).
3. Copy your repository's SSH URL (e.g., `git@github.com:your-username/your-repo.git`).

---

### **4. Run Gitfiti to Generate Commits**
Run the Gitfiti script to generate the commit history:

```sh
python gitfiti.py
```
This will generate a file called `gitfiti.sh`.

---

### **5. Move the Script & Initialize Git**
Move the script to your working directory:

```sh
mv gitfiti.sh ~/Documents/GitHub/
cd ~/Documents/GitHub/
```
Initialize a new Git repository:

```sh
git init
git remote add origin git@github.com:your-username/your-repo.git
```

---

### **6. Run the Generated Script**
Now, run the script to generate the commits:

```sh
sh gitfiti.sh
```
This will create a commit history that forms your artwork.

---

### **7. Push to GitHub**
Once complete, push your changes to GitHub:

```sh
git add .
git commit -m "Added GitHub contribution art"
git push -u origin main
```

🎉 **Done!** Go to your GitHub profile, and you should see your custom contribution artwork appear within a few minutes.

---

## 🛠 **Troubleshooting**

### **"Permission denied (publickey)" Error?**
This means you haven’t set up SSH authentication with GitHub.

#### **Fix:**
1. Check if you have an SSH key:
   ```sh
   ls ~/.ssh/id_rsa.pub
   ```
   - If you see a file, skip to Step 3.
   - If not, generate one:
     ```sh
     ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
     eval "$(ssh-agent -s)"
     ssh-add ~/.ssh/id_rsa
     ```

2. Copy your SSH key:
   ```sh
   cat ~/.ssh/id_rsa.pub | pbcopy  # macOS
   cat ~/.ssh/id_rsa.pub | clip    # Windows
   ```
   On Linux, manually copy the output from:
   ```sh
   cat ~/.ssh/id_rsa.pub
   ```

3. Add it to GitHub: [SSH Keys](https://github.com/settings/keys)
4. Test it:
   ```sh
   ssh -T git@github.com
   ```
   If it says **"Hi <your-username>! You've successfully authenticated"**, you're good to go!

---

## 🎭 **Customization**
Want to create your own custom artwork? Use an [online GitHub Contribution Graph Editor](https://github.com/jasonlong/gitfiti) to design your pattern, then generate the necessary commit script.

---

## ⭐ **Contribute**
Feel free to open a pull request if you improve this project!

📌 **Star this repo if you found it useful!** ⭐
