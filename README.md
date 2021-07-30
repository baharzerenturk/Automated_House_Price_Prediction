# Automated_House_Price_Prediction

![property-investment](https://user-images.githubusercontent.com/73841520/127619871-30b972f8-b354-484e-ac4f-0c628ed6c0ab.jpg)

## İş Problemi
Her bir eve ait özelliklerin ve ev fiyatlarının bulunduğu veriseti kullanılarak, farklı tipteki evlerin fiyatlarına ilişkin bir makine öğrenmesi projesi gerçekleştirilmek istenmektedir.

## Veri Seti Hikayesi
Ames, Lowa’daki konut evlerinden oluşan bu veriseti içerisinde 79 açıklayıcı değişken bulunduruyor.

Veri seti bir kaggle yarışmasına ait olduğundan dolayı train ve test olmak üzere iki farklı csv dosyası vardır.

Test veri setinde ev fiyatları boş bırakılmış olup, bu değerleri bizim tahmin etmemiz beklenmektedir.

## Değişkenler

Kategorik Değişkenler: <br/>
 'MSZoning' : Satışın genel imar sınıflandırmasını belirler. <br/>
 'Street' : Mülke bağlı caddenin doğrusal ayakları (Grvl: Çakıl, Pave: Döşeli) <br/>
 'Alley' : Mülke geçit erişimi türü (Grvl: Çakıl, Pave: Döşeli, NA: Geçit erişimi yok) <br/>
 'LotShape' : Mülkün genel şekli (Reg: Düzenli, IR1: Biraz düzensiz, IR2:Orta derecede düzzensiz, IR:Düzensiz) <br/>
 'LandContour' : Mülkün düzlüğü (Lvl: Yere yakın,Bnk: Sokak seviyesinden yüksekte, HLS: Eğimli, Low: Düşük seviyede) <br/>
 'Utilities' : Kullanılabilir yardımcı program türleri (gaz, elektrik vs) <br/> 
 'LotConfig' : arsa sınıflandırması (Inside: iç kısımda, Corner: köşede, CulDSac: çıkmaz sokak, FR2: iki cepheli, FR3: üç cepheli) <br/>
 'LandSlope' : mülkün eğimi (Gtl: Hafif, Mod: Orta, Sev: Şiddetli) <br/>
 'Condition1' : Çeşitli koşullara yakınlık <br/>
 'Condition2' : Çeşitli koşullara yakınlık (birden fazla varsa) <br/>
 'BldgType' : konut tipi <br/>
 'HouseStyle' : konut tarzı <br/>
 'RoofStyle' : çatı tipi <br/>
 'RoofMatl' : çatı malzemesi <br/> 
 'Exterior1st' : evin dış kaplaması <br/>
 'Exterior2nd' : Evin dış kaplaması (birden fazla malzeme varsa) <br/>
 'MasVnrType' : Duvar kaplama tipi <br/>
 'ExterQual' : Dış cephedeki malzemenin kalitesini değerlendirir <br/>
 'ExterCond' : Dış cephedeki malzemenin mevcut durumunu değerlendirir <br/>
 'Foundation' : yapının türü <br/>
 'BsmtQual' : Bodrumun yüksekliğini değerlendirir <br/>
 'BsmtCond' : Bodrumun genel durumunu değerlendirir <br/>
 'BsmtExposure' : bahçe seviyesindeki duvarları ifade eder <br/>
 'BsmtFinType1' : Bodrum bitmiş alanın değerlendirmesi <br/>
 'BsmtFinType2' : Bodrum bitmiş alanın değerlendirmesi (birden fazla tip varsa) <br/>
 'Heating' : Isıtma türü <br/>
 'HeatingQC' : Isıtma kalitesi ve durumu <br/>
 'CentralAir' : Merkezi klima <br/>
 'Electrical' : Elektrik sistemi <br/>
 'KitchenQual' : mutfak kalitesi <br/>
 'Functional' : Ev işlevselliği (Kesintiler garanti edilmediği sürece tipik olduğunu varsayın) <br/>
 'FireplaceQu' : şömine kalitesi <br/>
 'GarageType' : garaj konumu <br/>
 'GarageFinish' : garaj iç dekorasyonu <br/>
 'GarageQual' : garaj kalitesi  <br/>
 'GarageCond' : garaj durumu <br/>
 'PavedDrive' : asfalt yol <br/>
 'PoolQC' : havuz kalitesi <br/>
 'Fence' : çit kalitesi <br/>
 'MiscFeature' : Diğer kategorilerde kapsanmayan çeşitli özellikler <br/>
 'SaleType' : satış tipi <br/>
 'SaleCondition' : satış durumu <br/>
 'OverallCond' : Evin genel durumunu değerlendirir <br/>
 'BsmtFullBath' : Bodrum katı banyoları <br/>
 'BsmtHalfBath' : Bodrum küçük banyoları <br/>
 'FullBath' : zemin üzerindeki katlardaki banyolar <br/>
 'HalfBath' : zemin üzerindeki küçük banyolar <br/>
 'BedroomAbvGr' : zemin üzerindeki katlardaki toplam yatak odası sayısı (bodrum katı yatak odaları dahil DEĞİLDİR) <br/>
 'KitchenAbvGr' : zemin üzerindeki katlardaki toplam mutfak sayısı <br/>
 'Fireplaces' : şömine sayısı <br/>
 'GarageCars' : Araba kapasiteli garajın büyüklüğü <br/>
 'YrSold' : Konutun satıldığı yıl <br/>

Numerik Değişkenler: <br/>
 'Id', <br/>
 'MSSubClass' : satılacak konut türünü tanımlar (dublex ve aile için tek katlı vs..) <br/>
 'LotFrontage' : mülke bağlı cadde sayısı <br/>
 'LotArea' : metrekare cinsinden arsa büyüklüğü <br/>
 'OverallQual' : evin genel malzemesinin ve son halinin değerlendirilmesi <br/>
 'YearBuilt' : evin yapım tarihi <br/>
 'YearRemodAdd' : evin tadilat gördüğü tarih (tadilat görmemişse, evin yapım tarihi ile aynıdır.) <br/>
 'MasVnrArea' : Metrekare cinsinden duvar kaplama alanı  <br/>
 'BsmtFinSF1' : Tip 1 bitmiş metrekare <br/>
 'BsmtFinSF2' : Tip 2 bitmiş metrekare <br/>
 'BsmtUnfSF' : Bitmemiş metrekarelik bodrum alanı <br/>
 'TotalBsmtSF' : Bodrum alanının toplam metrekaresi <br/>
 '1stFlrSF' : Birinci kat metrekaresi <br/>
 '2ndFlrSF' : İkinci kat metrekaresi <br/>
 'LowQualFinSF' : Düşük kaliteli bitmiş fit kare (tüm katlar) <br/>
 'GrLivArea' : zemin üzerindeki toplam yaşam alanı metrekaresi <br/>
 'TotRmsAbvGrd' : zemin üzerindeki toplam oda sayısı (banyolar dahil değil) <br/>
 'GarageYrBlt' : Garajın yapıldığı yıl <br/> 
 'GarageArea' : garajın metrekare cinsinden büyüklüğü <br/>
 'WoodDeckSF' : Metrekare cinsinden ahşap güverte alanı <br/>
 'OpenPorchSF' : Metrekare cinsinden açık sundurma alanı <br/>
 'EnclosedPorch' : Metrekare cinsinden kapalı sundurma alanı <br/>
 '3SsnPorch' : Metrekare olarak üç mevsim sundurma alanı <br/>
 'ScreenPorch' : Metrekare cinsinden cam kaplı sundurma alanı <br/>
 'PoolArea' : Havuz alanı metrekaresi <br/>
 'MiscVal' : çeşitli diğer özelliklerin getirdiği değer (dolar) <br/>
 'MoSold' : konutun satıldığı ay <br/>
 'SalePrice' : mülkün satış değeri (dolar) <br/>

Kardinal Değişkenler <br/>
 'Neighborhood' : Mahalle <br/>
