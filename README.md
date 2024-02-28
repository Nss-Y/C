#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int ziyaretci_sayisi = 0;
    char devam;

    // Rastgele sayı üretmek için tohumlama
    srand(time(NULL));

    printf("Web sitesi ziyaretçi sayısını takip etmeye başladık!\n");

    do {
        // Yeni bir ziyaretçi ekle
        ziyaretci_sayisi += rand() % 10;

        printf("Şu anki ziyaretçi sayısı: %d\n", ziyaretci_sayisi);

        printf("Başka ziyaretçi eklemek istiyor musunuz? (E/H): ");
        scanf(" %c", &devam);
    } while(devam == 'E' || devam == 'e');

    printf("Program sonlandırıldı. Güncel ziyaretçi sayısı: %d\n", ziyaretci_sayisi);

    return 0;
}
