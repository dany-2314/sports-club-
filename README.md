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
    Sub Main()

        Dim Name As String
        Dim ID As String

        FileOpen(1, "C:\Users\dany\Desktop\Programs\Sports Club\Members.txt", OpenMode.Input)
        While Not EOF(1)
            Input(1, Name)
            Input(1, ID)



            Console.WriteLine("Member Name :" & Name)
            Console.WriteLine("Member ID :" & ID)
        End While

        FileClose(1)


        Console.ReadKey()
    End Sub
        Sub Main()

        Dim Name As String
        Dim ID As String
        Dim Found As Boolean = False
        Dim SearchName As String
        Dim upper As String = "searchname"
        Dim lower As String = "SEARCHNAME"

        FileOpen(1, "C:\Users\dany\Desktop\Programs\Sports Club\Members.txt", OpenMode.Input)
        Console.WriteLine("Search Name:  ")
        SearchName = Console.ReadLine

        Name = UCase(SearchName)
        Name = LCase(SearchName)
        SearchName = UCase(Name)
        SearchName = LCase(Name)

        While Not EOF(1)
            Input(1, Name)
            Input(1, ID)


            If Name = SearchName Then
                Found = True
                Console.WriteLine("Member Name :" & Name)
                Console.WriteLine("Member ID  :" & ID)

            End If
        End While
        FileClose(1)

        If Found = False Then Console.WriteLine("Record not found")


        Console.ReadKey()

    End Sub
    Sub Main()
        Dim Name As String
        Dim ID As String
        Dim More As String
        Dim stup As Boolean = False


        Do Until More = "N" Or More = "n"

            Console.Write("Name of Member: ")
            Name = Console.ReadLine


            Console.Write("ID of Member: ")
            ID = Console.ReadLine


            Console.WriteLine("If No More Members press:N Otherwise press:Y")
            More = Console.ReadLine

            If More = "N" Or More = "n" Or More = "Y" Or More = "y" Then
                stup = True
            Else : Console.WriteLine("Error")
                End

            End If
        Loop

        WriteLine(1, Name)
        WriteLine(1, ID)
        FileOpen(1, "C:\Users\dany\Desktop\Programs\Sports Club\Members.txt", OpenMode.Append)


        FileClose(1)

        Console.ReadKey()

    End Sub
      Sub Main()
        Dim Name As String
        Dim ID As String
        Dim telephone As String
        Dim startDate As String
        Dim Updated As String
        Dim found As Boolean = False


        FileOpen(1, "C:\Users\dany\Desktop\Programs\Sports Club\Members.txt", OpenMode.Input)
        FileOpen(2, "C:\Users\dany\Desktop\Programs\Sports Club\temp.txt", OpenMode.Output)
        Console.Write("Name of Member that needs to be updated: ")
        Updated = Console.ReadLine
        Name = UCase(Updated)
        Name = LCase(Updated)
        Updated = UCase(Name)
        Updated = LCase(Name)


        While Not EOF(1)
            Input(1, Name)
            Input(1, ID)


            If Name = Updated Then
                found = True
                Console.WriteLine("Member Name :" & Name)
                Console.WriteLine("Member ID  :" & ID)
                Console.Write("telephone number?: ")
                telephone = Console.ReadLine
                Console.Write("Starting date: ")
                startDate = Console.ReadLine

                WriteLine(2, Name)
                WriteLine(2, ID)
                WriteLine(2, telephone)
                WriteLine(2, startDate)

            End If
        End While


        If found = False Then Console.WriteLine("Record not found")



        FileClose(1)
        FileClose(2)
        My.Computer.FileSystem.DeleteFile("C:\Users\dany\Desktop\Programs\Sports Club\Members.txt")
        My.Computer.FileSystem.RenameFile("C:\Users\dany\Desktop\Programs\Sports Club\temp.txt", _
                                          "Members.txt")


        Console.ReadKey()




       

    End Sub
