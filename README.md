# sports-club-
  Sub Main() 

        Dim Name As String
        Dim ID As String
        Dim More As String
        Dim stup As Boolean = False

        FileOpen(1, "C:\Users\dany\Desktop\Programs\Sports Club\Members.txt", OpenMode.Output)

        Do Until More = "N" Or More = "n"

            Console.Write("Name of Member: ")
            Name = Console.ReadLine
            WriteLine(1, Name)

            Console.Write("ID of Member: ")
            ID = Console.ReadLine
            WriteLine(1, ID)

            Console.WriteLine("If No More Members press:N Otherwise press:Y")
            More = Console.ReadLine

            If More = "N" Or More = "n" Or More = "Y" Or More = "y" Then
                stup = True
            Else : Console.WriteLine("Error")
                End

            End If

        Loop




        FileClose(1)

        Console.ReadKey()
    End Sub
