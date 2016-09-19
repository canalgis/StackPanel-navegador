# StackPanel-navegador
Crear aplicación para navegar en Internet con StackPanel


using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Runtime.InteropServices.WindowsRuntime;
using Windows.Foundation;
using Windows.Foundation.Collections;
using Windows.UI.Xaml;
using Windows.UI.Xaml.Controls;
using Windows.UI.Xaml.Controls.Primitives;
using Windows.UI.Xaml.Data;
using Windows.UI.Xaml.Input;
using Windows.UI.Xaml.Media;
using Windows.UI.Xaml.Navigation;

// The Blank Page item template is documented at http://go.microsoft.com/fwlink/?LinkId=402352&clcid=0x409

namespace App16
{
    /// <summary>
    /// An empty page that can be used on its own or navigated to within a Frame.
    /// </summary>
    public sealed partial class MainPage : Page
    {
        public MainPage()
        {
            this.InitializeComponent();
            MyFrame.Navigate(typeof(Page1));
        }

        private void HomeButton_Click(object sender, RoutedEventArgs e)
        {
            MyFrame.Navigate(typeof(Page2));
        }

        private void BackButton_Click(object sender, RoutedEventArgs e)
        {
            if (MyFrame.CanGoBack)
            {
                MyFrame.GoBack();
            }
        }






<Page
    x:Class="App16.Page1"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:local="using:App16"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <StackPanel>
        <TextBlock FontSize="48" Text="Pagina 1" />
        <HyperlinkButton Content="Go to Pagina 2 " Click="HyperlinkButton_Click"/>
        <HyperlinkButton Content=" Go to FCA en Linea.unam.mx" NavigateUri="http://fcaenlinea.unam.mx/licenciaturas/informatica/" />
    </StackPanel>
</Page>






<Page
    x:Class="App16.Page2"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:local="using:App16"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <StackPanel>
        <TextBlock FontSize="48" Text="Pagina 2"/>
        <HyperlinkButton Content="Go to Pagina 1 " Click="HyperlinkButton_Click"/>
        <HyperlinkButton Content=" Go to FCA en Linea.unam.mx" NavigateUri="http://fcaenlinea.unam.mx/licenciaturas/informatica/" />

    </StackPanel>
</Page>
