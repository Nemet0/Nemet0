function register() {
    // İstifadəçi adı və şifrə məlumatlarını əldə et
    const username = document.getElementById("username").value;
    const password = document.getElementById("password").value;

    // Məlumatlar yoxlanır
    if (username && password) {
        alert("Qeydiyyat uğurla tamamlandı!");

        // Qeydiyyat bölməsini gizlədərək seçimlər bölməsini göstəririk
        document.getElementById("register-section").style.display = "none";
        document.getElementById("options-section").style.display = "block";
    } else {
        alert("Zəhmət olmasa istifadəçi adı və şifrə daxil edin.");
    }
}

function showInfo(category) {
    let info = document.getElementById("info");

    // Seçilən kateqoriyaya uyğun məlumat
    if (category === "biznes") {
        info.textContent = "Biznes sahəsi sahibkarlıq, maliyyə və idarəetmə ilə bağlı mövzuları əhatə edir.";
    } else if (category === "it") {
        info.textContent = "IT sahəsi proqramlaşdırma, texnologiya və informasiya təhlükəsizliyi mövzularını əhatə edir.";
    } else if (category === "tibb") {
        info.textContent = "Tibb sahəsi sağlamlıq, tibbi araşdırmalar və xəstəliklərin müalicəsi ilə bağlıdır.";
    }
}
