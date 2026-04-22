# Library
Library for storing books
#Small library project in python#
def library():
    while True:
        print("Menue")
        print("1.Add Book")
        print("2.Show Books")
        print("3.Issue Book")
        print("4.Return Book")
        print("5.Exit")
        choice=int(input("Enter a number:"))
        if choice==1:
            add_book()
        elif choice==2:
            show_books()
        elif choice==3:
            issue_book()
        elif choice==4:
            return_book()
        elif choice==5:
            print("Thankyou")
            break
        else :
            print("Invalid choice")

book=[]
issued_books=[]
def add_book():
        name=input("Enter name of book")
        book.append(name)
        print(f"{name} book is added")

def show_books():
        if len(books)==0:
           print("No books avilable")
        else:
            print("Avilable Books")
            for book in books:
                print(book)
def issue_book():
    if len(books)==0:
           print("No books avilable")
    else:
        name=input("Book you want to issue")
        if name in books:
            issued_books.append(name)
            book.remove(name)
            print(f"{name} Book is issued")
        else :
            print(f"{name} book is not avilable")
    def return_book():
        name=input("Enter the book name:")
        if name in issue_book:
            issue_book.remove(name)
            book.append(name)
            print(f"{name} book is returned")
        else:
            print(f"{name} book doesn't issued by this library")

library()
