# Bekra.ImageDownload

Bekra.ImageDownload, .NET platformunda resim indirme işlemlerini kolaylaştırmak için oluşturulmuş bir kütüphanedir. Bu kütüphane ile resimleri belirtilen URL adreslerinden indirebilir ve kaydedebilirsiniz.

## Özellikler

- Resimleri belirtilen URL adreslerinden indirme.
- İndirilen resimleri belirtilen dosya adı ve formatla kaydetme.
- Geriye dönük uyumlu ve kolay kullanım.

## Nasıl Kullanılır

Aşağıda, Bekra.ImageDownload kütüphanesini kullanarak bir resmi nasıl indireceğinizi gösteren örnek bir kod bulunmaktadır:

```csharp
using System.Drawing.Imaging;
using BekraİmageDownload;

class Program
{
    static void Main()
    {
        string imageUrl = "https://4.bp.blogspot.com/-i5PEHve8n4k/Xghl14diB2I/AAAAAAAACaU/QaMj0LUoeV4iJCbNMSZJ399s7j7kKMMtwCK4BGAYYCw/s1600/Ads%25C4%25B1z.webp";
        string filename = "downloaded_image.jpg"; // İndirilen resmin dosya adı
        ImageFormat format = ImageFormat.Jpeg; // İndirilen resmin formatı

        using (ImageDownloader downloader = new ImageDownloader())
        {
            bool result = downloader.SaveImage(imageUrl, filename, format);

            if (result)
            {
                Console.WriteLine("Resim başarıyla indirildi ve kaydedildi.");
            }
            else
            {
                Console.WriteLine("Resim indirilirken bir hata oluştu.");
            }
        }
    }
}
```
<h2>Kurulum</h2>
<p>Bekra.ImageDownload'ı kullanmak için NuGet paketi olarak projenize ekleyebilirsiniz. Visual Studio'da Package Manager Console kullanarak aşağıdaki komutu çalıştırabilirsiniz:</p>

<pre><code class="language-bash">Install-Package Bekra.ImageDownload</code></pre>

<h2>Katkıda Bulunma</h2>
<p>Eğer bu projeye katkıda bulunmak veya hata bildirmek isterseniz, lütfen <a href="[https://github.com/yourusername/Bekra.ImageDownload](https://github.com/ebubekirbastama/Csharp_Image_Download)">Bekra.ImageDownload GitHub Deposu</a> adresini ziyaret edin.</p>

<h2>Lisans</h2>
<p>Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için <a href="LICENSE">LICENSE</a> dosyasına bakın.</p>
