# appveyor3
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace sum_of_numbers_in_a_string
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void btnExit_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void btnCalc_Click(object sender, EventArgs e)
        {
            
                
            string line=txtEnter.Text;                  //Reads numbers entered by user

            char[] delim = {','};                       //sets the delimeter as a comma

            string[] tokens = line.Split(delim);        //splits the entered string into tokens

            int total;                                  //adds the tokens together
            total = 0;
            foreach (string str in tokens)
            {
                total += int.Parse(str);
            }
            MessageBox.Show( "The total is: " + total.ToString());

                                                        //shows the total in a messagebox

        }
    }
}
