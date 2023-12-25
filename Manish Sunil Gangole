#include <stdio.h>
#include <string.h>

#define MAX_BOOKS 100
#define MAX_MEMBERS 100

typedef struct {
    int bookId;
    char title[100];
    char author[100];
    int available;
} Book;

typedef struct {
    int memberId;
    char name[100];
} Member;

typedef struct {
    Book books[MAX_BOOKS];
    Member members[MAX_MEMBERS];
    int bookCount;
    int memberCount;
} Library;

void addBook(Library* library, int bookId, const char* title, const char* author) {
    if (library->bookCount < MAX_BOOKS) {
        Book book = {bookId, "", "", 1};
        strncpy(book.title, title, sizeof(book.title) - 1);
        strncpy(book.author, author, sizeof(book.author) - 1);
        library->books[library->bookCount++] = book;
        printf("Book added successfully!\n");
    } else {
        printf("Maximum book capacity reached!\n");
    }
}

void addMember(Library* library, int memberId, const char* name) {
    if (library->memberCount < MAX_MEMBERS) {
        Member member = {memberId, ""};
        strncpy(member.name, name, sizeof(member.name) - 1);
        library->members[library->memberCount++] = member;
        printf("Member added successfully!\n");
    } else {
        printf("Maximum member capacity reached!\n");
    }
}

void issueBook(Library* library, int bookId, int memberId) {
    // Implement the issueBook function
}

void returnBook(Library* library, int bookId) {
    // Implement the returnBook function
}

void generateReport(Library* library) {
    // Implement the generateReport function
}

int main() {
    Library library = {{}, {}, 0, 0};

    printf("Welcome to the Library Management System!\n");

    while (1) {
        printf("\nPlease select an option:\n");
        printf("1. Add a book\n");
        printf("2. Add a member\n");
        printf("3. Issue a book\n");
        printf("4. Return a book\n");
        printf("5. Generate report\n");
        printf("6. Exit\n");

        int choice;
        scanf("%d", &choice);

        if (choice == 1) {
            int bookId;
            char title[100], author[100];

            printf("Enter book ID: ");
            scanf("%d", &bookId);

            printf("Enter book title: ");
            scanf("%s", title);

            printf("Enter book author: ");
            scanf("%s", author);

            addBook(&library, bookId, title, author);
        } else if (choice == 2) {
            int memberId;
            char name[100];

            printf("Enter member ID: ");
            scanf("%d", &memberId);

            printf("Enter member name: ");
            scanf("%s", name);

            addMember(&library, memberId, name);
        } else if (choice == 3) {
            int bookId, memberId;

            printf("Enter book ID: ");
            scanf("%d", &bookId);

            printf("Enter member ID: ");
            scanf("%d", &memberId);

            issueBook(&library, bookId, memberId);
        } else if (choice == 4) {
            int bookId;

            printf("Enter book ID: ");
            scanf("%d", &bookId);

            returnBook(&library, bookId);
        } else if (choice == 5) {
            generateReport(&library);
        } else if (choice == 6) {
            break;
        } else {
            printf("Invalid choice. Please try again.\n");
        }
    }

    printf("Thank you for using the Library Management System. Goodbye!\n");

    return 0;
}
