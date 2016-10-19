# CSharpPortfolio-JelleSwaelen

## Classes

### Public methods

Een public method kan wel aangeroepen worden van buiten de class waarin ze zich bevindt.

2016-02-20 Oefening Dobbelstenen

In de code hieronder is het dus makkelijk om _geefGetal_ uit te voeren, omdat de functie public is.
Als _geefGetal_ private zou zijn, kan ze niet aangeroepen worden buiten de class _DobbelsteenResultaat_.

```csharp
    public partial class MainWindow : Window
    {
        public DobbelsteenResultaat dobbel;
        public int getal;
        public int getal2;

        public MainWindow()
        {
            InitializeComponent();

            dobbel = new DobbelsteenResultaat();

        }

        private void btnGooiDobbelsteen_Click(object sender, RoutedEventArgs e)
        {
            lblGetal1.Content = Convert.ToString(dobbel.geefGetal());
            lblGetal2.Content = Convert.ToString(dobbel.geefGetal());

        }
    }

    public class DobbelsteenResultaat
    {
        Random rnd = new Random();
        Random rnd2 = new Random();

        public int geefGetal()
        {
            int getal = rnd.Next(1, 6);
            return getal;

        }

        public int geefGetal2()
        {
            int getal2 = rnd2.Next(1, 6);
            return getal2;
        }
    }
```