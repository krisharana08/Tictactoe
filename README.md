# Tictactoe

<!DOCTYPE html>


<html>
    <head>
        <title>Tic-Tac-Toe game</title>
        <link rel="stylesheet" href="bootstrap.min.css"/>
        <script>

            flag=1;
            function OX(bid)
            {
                var btn=document.getElementById(bid); 
              
                if(flag)
                {
                    btn.innerHTML="O";
                    flag=0;
                }
                else
                {
                    btn.innerHTML="X";
                    flag=1;
                }
                btn.className="btn btn-warning";
                btn.disabled=true;
                
                winner();
            }

            function winner()
            {   
               b1=document.getElementById("1");
               b2=document.getElementById("2");
               b3=document.getElementById("3");
               b4=document.getElementById("4");
               b5=document.getElementById("5");
               b6=document.getElementById("6");
               b7=document.getElementById("7");
               b8=document.getElementById("8");
               b9=document.getElementById("9");
                
                    if( b1.innerHTML!=""  && (b1.innerHTML==b2.innerHTML && b2.innerHTML==b3.innerHTML))
                         alert("You win the game "+b1.innerHTML);
                            
                     else if(b4.innerHTML!="" &&( b4.innerHTML==b5.innerHTML && b5.innerHTML==b6.innerHTML))
                          alert("You win the game "+b4.innerHTML);
                        
                     else if(b7.innerHTML!="" &&( b7.innerHTML==b8.innerHTML && b8.innerHTML==b9.innerHTML))
                          alert("You win the game "+b7.innerHTML);
                       
                     else if(b4.innerHTML!="" && ( b1.innerHTML==b4.innerHTML && b4.innerHTML==b7.innerHTML))
                          alert("You win the game "+b1.innerHTML);
                        
                     else if(b2.innerHTML!="" && ( b2.innerHTML==b5.innerHTML && b5.innerHTML==b8.innerHTML))
                         alert("You win the game "+b2.innerHTML);
                       
                     else if(b3.innerHTML!="" && ( b3.innerHTML==b6.innerHTML && b6.innerHTML==b9.innerHTML))
                         alert("You win the game "+b3.innerHTML);
                       
                     else if(b1.innerHTML!="" && ( b1.innerHTML==b5.innerHTML && b5.innerHTML==b9.innerHTML))
                         alert("You win the game "+b1.innerHTML);
                       
                     else if(b3.innerHTML!="" && ( b3.innerHTML==b5.innerHTML && b5.innerHTML==b7.innerHTML))
                         alert("You win the game "+b3.innerHTML);
                       
                     else if(tie(b1,b2,b3,b4,b5,b6,b7,b8,b9))
                         alert("Game over. game will be Tie...");
                        

                }
            function tie(b1,b2,b3,b4,b5,b6,b7,b8,b9)
            {
                if(b1.innerHTML!="" && b2.innerHTML!="" && b3.innerHTML!="" && b4.innerHTML!="" && b5.innerHTML!="" && b6.innerHTML!="" && b7.innerHTML!="" && b8.innerHTML!="" && b9.innerHTML!="" )
                 
                        return true;
                 
                else
                
                       return false;        
            }
        </script>
        <style>
            h1{
                padding-top:20px;
            }
            hr{
                height: 2px;
                background-color: aliceblue;
            }
           
        </style>
    </head>
    <body>
        <div class="container-fluied bg-dark text-light" style= "height:100%; padding-bottom: 10%;" >
            <h1 align="center">Tic-Tac-Toe Game</h1><br>
            <hr><br><br><br>
           <div class="container" style="padding-bottom: 10px;" >
                <div class="my-10" align="center">
                    <button type="button" id="1" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="2" name="" class="btn btn-info mx-3" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="3" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>

                </div>
                <div class="my-3" align="center">
                    <button type="button" id="4" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="5" name="" class="btn btn-info mx-3"  style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="6" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>

                </div>
                <div class="my-3" align="center">
                    <button type="button" id="7" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="8" name="" class="btn btn-info mx-3" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>
                    <button type="button" id="9" name="" class="btn btn-info" style="height: 100px; width: 100px;" onclick="OX(this.id)"></button>

                </div>

           </div>
           <a href="tic-tac.html">
           <center><button tyle="button" class="btn btn-warning btn-lg" align="center" style="margin-top: 5%;">Restart</button></center>
        </a>
        </div>
    </body>
</html>
