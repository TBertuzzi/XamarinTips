# XamarinTips

Repositorio com dicas para coisas simples com Xamarin

[![GitHub contributors](https://img.shields.io/github/contributors/TBertuzzi/XamarinTips.svg)](https://github.com/TBertuzzi/XamarinTips/graphs/contributors)

# Xamarin.Forms

### Forçar o Tema ou Alterar o tema padrão 

```csharp
  Application.Current.UserAppTheme = OSAppTheme.Dark;
```

```csharp
  Application.Current.RequestedThemeChanged += Current_RequestedThemeChanged;
  
   private void Current_RequestedThemeChanged(object sender, AppThemeChangedEventArgs e)
        {
            if (e.RequestedTheme == OSAppTheme.Dark)
                Application.Current.UserAppTheme = OSAppTheme.Dark;
            else
                Application.Current.UserAppTheme = OSAppTheme.Light;
        }
  
```

# Xamarin.Android

### Forçar Tema no Android

Mude o estilo da MainTheme.Base para 
```csharp
<style name="MainTheme.Base" parent="Theme.AppCompat.DayNight.DarkActionBar">
```

### Encontrar o Arquivo .keystore para assinar o Android 

Considerando a instalação Padrão :

***Windows : C:\Usuários\NOMEDEUSUÁRIO\AppData\Local\Xamarin\Mono for Android\debug.keystore***
***Mac : ~/.local/share/Xamarin/Mono for Android/debug.keystore***

Arquivos criados por você :

***Windows : C:\UserNAME UserData\Local\Xamarin\Mono\para Android Keystorealias\alias.keystore***
***Mac : ~/Library/Developer/Xamarin/Keystore/alias/alias.keystore***

onde alias é o nome do certificado que você criou



# Xamarin.iOS

### Forçar Tema no iOS 

no info.plist adicionar :

```csharp
<key>UIUserInterfaceStyle</key>
<string>Light</string>
```

### Este Repositorio esta em desenvolvimento .. ;)

Pull Requests são bem vindos :D
