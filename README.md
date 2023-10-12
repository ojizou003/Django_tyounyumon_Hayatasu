# 「 Django 超入門」はやたす youtube

2023/10/12 ~ 10/13

## コースの紹介と Django のインストール

Djangoとは、PythonでWebアプリを開発するためのフレームワーク

データベースにテーブルを作成するときも、SQLを書くのではなく、Pythonのクラスを使って定義

仮想環境の作成  

- cdに移動
- conda activate base
- virtualenv venv ..venvフォルダの作成
- venv\Scripts\activate ..仮想環境の有効化

## Djangoプロジェクトの開始と初期設定

【用語】  
Djangoプロジェクト≒Webアプリケーション  
Djangoアプリケーション≒Webアプリケーションにおける個別の機能  

プロジェクトの開始  
``` django-admin startproject プロジェクト名 . ```  
--> プロジェクト名フォルダとmanage.pyが作成される  

manage.py の中身は触らす、コマンドの実行のみに使用  

サーバーの起動  
``` python manage.py runserver ```  

サーバーの停止  
    Ctrl ＋ C  

アプリケーションの作成  
``` python manage.py startapp アプリケーション名 ```  
    --> アプリケーション名のフォルダが作成される

初期設定  
Djangoを日本語化  
    プロジェクトフォルダ内のsettings.py  
    LANGUAGE_CODEを変更 --> "ja"  
    TIME_ZONE --> "Asia/Tokyo"  

プロジェクトに作成したアプリケーションの情報を紐づけ  
    プロジェクトフォルダ内のsettings.py  
    INSTALLED_APPSにアプリケーションを追加  
    ``` "blog.apps.BlogConfig", ``` ..ex) アプリケーションblogを作成した場合

## モデルの定義とテーブルの作成

Djangoでデータベースを扱う手順

1. models.py でモデルを定義
2. マイグレーションファイルを作成
3. データベースのテーブルに反映

モデルの定義  
``` class クラス名(models.Model): ```  

マイグレーションファイルの作成  
ターミナルで``` pytyon manage.py makemigrations ```  

データベースのテーブルに反映  
ターミナルで``` python manage.py migrate ```

---

動画ここまで...  
