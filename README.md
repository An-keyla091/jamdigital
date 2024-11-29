import tkinter as tk
from time import strftime

def update_time():
    current_time = strftime('%H:%M:%S')  # Format jam:menit:detik
    label.config(text=current_time)
    label.after(1000, update_time)  # Update setiap 1 detik

# Membuat jendela aplikasi
root = tk.Tk()
root.title("Jam Digital")

# Menambahkan label untuk menampilkan waktu
label = tk.Label(root, font=('Arial', 50), background='black', foreground='white')
label.pack(anchor='center')

# Menjalankan fungsi update_time
update_time()

# Memulai aplikasi
root.mainloop()
