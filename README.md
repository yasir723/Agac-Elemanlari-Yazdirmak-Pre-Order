# Ağaç Elemanları Yazdırmak (Pre-Order)
Genelde Ağaç veri yapısında bulunan elemanları yazdırmak için Pre-Order yöntemini kullanarak yazdırılır.
`Pre-Order gezinme algoritması: ` her bir düğümün değerini önce kendisi, ardından sol alt ağaç ve en sonunda sağ alt ağaç olarak sırayla yazdırır.


Bu C# sınıfı, binary ağaç veri yapısını oluşturmak için kullanılır
## `tree` Sınıfı

```csharp
class tree
{
    public int value;
    public tree right;
    public tree left;
}
```

### Özellikler

- `value`: Düğümün değerini temsil eder.
- `right`: Düğüme bağlı olan sağ alt düğümü belirtir.
- `left`: Düğüme bağlı olan sol alt düğümü belirtir.

## `yazdır` Metodu
```csharp
static void yazdır(tree node)
{
    if (node == null) return;

    Console.WriteLine(node.value);

    yazdır(node.left);
    yazdır(node.right);
}
```

## Parametreler

- `node`: Ağaçtaki mevcut düğüm.

## Avantaj

- En yaygın yazdırma algoritması ve ağaçtaki elemanlar `okunabilir basit` bir şekilde yazdırmayı sağlar.

## İşleyiş
1. İlk olarak gönderilen ağaç null ise, null döndürülür.
2. Null değilse, mevcut düğümün değeri yazdırılır.
3. Yazdırıldıktan sonra sola düğüme geçilir.
4. Ve yine sola gitmeye devam edilir, null değer alana kadar.
5. En sola gidildiğinde null döndürülür ve bu sefer en solun sağına gidilir ve taşıdığı değer yazdırılır.
6. Kök düğümün sol tarafı tamamlandıktan sonra kök düğümün sağ tarafına gidilir ve aynı işlem tekrarlanır.

<div align="center">
    <h3>Binary Ağaç Elemanları Pre-Order Yazdırma Aşamaları</h3>
</div>

[![Yazdırma Adımları](https://github.com/yasir723/Agac-Elemanlari-Yazdirmak-Pre-Order-/assets/111686779/17d9ed6a-9a5b-4e64-a13f-d2312161d337)](https://github.com/yasir723/Agac-Elemanlari-Yazdirmak-Pre-Order-/assets/111686779/b8d06cfc-8fef-4c9d-aaf1-9fa3dff99040)


